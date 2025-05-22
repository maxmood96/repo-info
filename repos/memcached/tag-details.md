<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:1-alpine3.21`](#memcached1-alpine321)
-	[`memcached:1-bookworm`](#memcached1-bookworm)
-	[`memcached:1.6`](#memcached16)
-	[`memcached:1.6-alpine`](#memcached16-alpine)
-	[`memcached:1.6-alpine3.21`](#memcached16-alpine321)
-	[`memcached:1.6-bookworm`](#memcached16-bookworm)
-	[`memcached:1.6.38`](#memcached1638)
-	[`memcached:1.6.38-alpine`](#memcached1638-alpine)
-	[`memcached:1.6.38-alpine3.21`](#memcached1638-alpine321)
-	[`memcached:1.6.38-bookworm`](#memcached1638-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.21`](#memcachedalpine321)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:0f92cdf1ca059c3b747f95328ed9e8de40866896657cb2b73148be36331efc02
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

### `memcached:1` - linux; amd64

```console
$ docker pull memcached@sha256:15c127398e9bb6bdfdbd6689b817964617401f2d9ca294758323011b3bb09350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33021901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f40f7fb4f0d5e586a146a0a994596292ea1e784ca1657eed1192b2fe17a003c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62639a9e53d980a0e86e3b54ae34e1e913a7f6cebd1bce7741e629047b732896`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5783d9aa8a04d558f9d1d5407d3f6dddb064b0a670738a5cbc480866bbc1a30`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.5 MB (2492219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609bfa774ee059a5d07cc14920af077ac7de9039c567f38164ea31f5eb04d3ba`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.3 MB (2302838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062ee789e2fd31345a9db851ddb0616c67ac7a4ea84e3a0e953af88faa98e3e5`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8416b27aabc571df320856a2ff533825bcbfc2fa602782561ff6b1a0449b821`  
		Last Modified: Wed, 21 May 2025 23:16:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:7b5eaaa81772b0dc7377f0c8a8d41bb09c38c1a07292c0e0bef5654ceef3a28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c8287d2eb936f10093c74288a99d09a35c07df6033435ba68847dba2b0fdff`

```dockerfile
```

-	Layers:
	-	`sha256:f5c222a0451ee4a8115a7a9421176131c1481dd511e4ec028e050fdf94e7b741`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.3 MB (2308990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01ac10f70adef13c64045d3be5956b00caafe800e1fab7640f6eaa5f9ea66864`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:9d0d272209b7fd9922e4184de83ab429d527ad56c2f92a6a262cb88cf331551e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30087755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8113ec8739204304b1054312c93717e8c84189d23a003648ffa966d472462cad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01741d1d3bd96678d0f5dccb883892b5af0a3ffb6fe1abaf71cfa8d27579819`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e33674278ab7a59427b75a5c5a4fc74379bdc2cea1105e212becedfd13aadc`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.1 MB (2097064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c00b2be2834a255d33718d0903d2637ed005c981ee3d72a52654f7e0aed5e78`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.2 MB (2232281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148a70549f08f93b07f1c60ad72af807c88405d06687d9fe374648b9a484d40e`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93adc89552cc46d51abc366499a6fac900badfa05b8a0c8c604a7e4ac0cae40`  
		Last Modified: Wed, 21 May 2025 23:46:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:7659c54d461b01b9e2062f0a8843b75b7d6a793c3d358a339b78e071770dcbd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2338302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af770cd911aab0856b542fdf7bc835ddf01b1ce26aa176b7b9cacfbc9388fb2d`

```dockerfile
```

-	Layers:
	-	`sha256:6d50a9e0dd879a75ce6c9396bd03c5ecb9beefd32a2d5bd6cf54f36341327685`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.3 MB (2312836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f3107fa09f2c0b66f32bebd5a1bb01208c84b9fa1da768bf5a5dbd20ca500d0`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:95630a66e2d5c3a453ccc0f22d18ce0a297f1f21536938ff8f1b93c86b9cfbea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28065225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127e001dab188acb98ae7340be866c4c3ae686a9285cf40bd10f9dc702a73ee9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b5a50ba24d961f5862446c5e48fe0c5dbf9acfb0a3718255dd76fab71e84a7`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4adc063a4b96db7c50bcc78cd236a7102a3c31a61fb4216967b2cdcab50c24`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 1.9 MB (1946317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26fc15d35761b3f0c7797ea1ffc39ab51d4227089df7d6b5d2a075730795d20`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 2.2 MB (2184474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64f51527fd9673b0b39f52e4d608185f9461b4282e581e5ef1ce245bdc451e8`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138b4847c3beba31cf3c1807f17ce0b970ec15f04604f92ac076ff994c1a0f68`  
		Last Modified: Wed, 21 May 2025 23:49:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:2f6b92592e3f57dbba3221b48b0dce566be344c3e646a89421cfc68ac2827925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857e0ef0a015c3e4c292fe0a24e960bbfba6c8f5844e8022a8d5c11a52d798c8`

```dockerfile
```

-	Layers:
	-	`sha256:7fb0e5e8b1ea53e4ba20b1cee752d37de3b49eaa2c057aea103fb67ad94a2cf5`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 2.3 MB (2311273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:210181bb919654e239b27e79e0a1003bde8ec7d3dd27841dfb0f95d0c62d23d4`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4fc35e2dfad1e5506199e79f54d5400afd22aee2bb1fe0b5e554d051c7c38d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32711358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d9217ce2913b829164781088c527a86fb1d43a48403bfd92c09a9ce7fd4c95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661e0135b0352aad675030e66bdddcf402a36cea02deb2532b0a24d5ba27554`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e7084e0aea669193e1cab086c096bd0764a05f1bf138e1f7c8f0c04eaf3b52`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.4 MB (2355810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259807b0c15878094bf0f3b13afedc0ef32d7eb679af66072ae18096127d72e1`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.3 MB (2288755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacab3ed6c99f53a622eefcda0dee8f57e377bfb97e7f57674e5030b7172988c`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12316079cc5378e29c63fc769e3686207ce41caec7ed76e8e5bb2c3e3b9a4938`  
		Last Modified: Thu, 22 May 2025 00:10:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:ed76bdc15573ee04e086b0a05bfe7056bb260ef0625d8fca2b4c89bd490db508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282362d3d316c5b5bd6b78ff5cfdd9be97d18c3c0018244eeac32f5a123b7d24`

```dockerfile
```

-	Layers:
	-	`sha256:f50a38ae76734a0eff8b24f4e99acd0d1bdb9ab848e04f9ddbcdcf08aadbe908`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.3 MB (2309305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ec44f0bfbd8d8065048e9d7bc8c90c0dcc460586efa613acacb43cb444f3c91`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 25.5 KB (25516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:427a7ad7f639e7cbf4161751cad9450044cbfaf6be8180abc51e01f68cad186c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33962949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a7e05a07d6b637c8752b13cee1ed7a5ebe2a4ef846c0eecaf4b7904d07ff4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d0594fdf9f07f23d90458a489d7972ab011bc5cca342af82850c3e9c024e3e`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4797e4e934c0c059a34c8b9d6c2adc40dece3f2ba61185edfa1c36591ef3549f`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.5 MB (2502658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7cc241a1440cfefd9f5b88cb6233b9ee820398da0c74155859c3114dd0646c`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.3 MB (2251292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cacd3ce01b0221992568e7179a1408774519b7dfbfc1daf37095764ae9bf16`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4abb18b4fabd731df2a3dbba62cd3f6de6cc4a6ab8419827bcbeb87641c4ad7`  
		Last Modified: Wed, 21 May 2025 23:16:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:3c7de609f262a2ab1ddafedf272ac08f1eded0a2b08450f76dbd927b4b746f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfd69fc1ff5ceb8e449d8374c86427aafe41200a46c937aee60fce7a21ebf13`

```dockerfile
```

-	Layers:
	-	`sha256:87803ae24543fc1d1ecf0d1af68207e9714fd56829bab2354f9dd3940e3cf240`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.3 MB (2306133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b6feaf94b04b7737bdbf12b7c3f15ea0f7c46ead6614b9a46a82b87b5e5c75`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:55e7557e19928aa1991fbb59dcb75ea75b5b87115b772f36fd7302618c031468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32774540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1d55a83743e8701a5f0aacd60bd4260744537318e9335e6f681f765a2f536e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Wed, 21 May 2025 22:28:22 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00be87e076613598c61cb34d1eab1a04e74cb16c312c6b2737aaa5b2f54f0cad`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4fdba1c45e7b51399330c05d6b7e619f96cc0ed80cfd6bc75722cf5c982105`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 1.9 MB (1944079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d0d8b3f93dba36eb05fef21a3cda9faaf4e064e161fb87965839f9da4a2a20`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 2.3 MB (2317092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d4a6285da352b0857160c9194204e6801269736b4b18ca39bead26e9be8345`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d044aab1c575f4ebf7752dd0c9d988fc02e7b6f86316622b1678cea3cb9ca44`  
		Last Modified: Thu, 22 May 2025 00:11:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:048fdf15ee7c39e63ec03618e8587191e3915649f1b0076574f19773f9ccf067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c546fba658eb64c00d4036d1ac6c25e4a6f0b1681950c03a94ffc3954fb0d5c9`

```dockerfile
```

-	Layers:
	-	`sha256:2d39a6be744c7e579e7d4147fdc82a19956c6223fcb98601955e9a0a5d1e9e2e`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 25.2 KB (25216 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:3e871b866378795839b5bac555437a97646aa6f1c2abccdd182fe6b8ea84c983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37197690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9129b120bccf4a13f93ae0e47a4046e9ab94b4ff2d8de473eb248683b2802a6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Wed, 21 May 2025 22:28:16 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50fa062d3f9b2ead925a10e36e54327c0aae0c280d34e1075bcf82708310f13`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c345e70ea367cfeb023138dcae0d694e941f247957111430bd191f08181ef2b`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.7 MB (2710200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bd27f00915f27350ad09f9ca295e22cc787fe09c28db9040ad1bfcbfb1508d`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.4 MB (2419066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eee08866234c70e5aa7c719d396e45b9f8955b9a790d0654fd365d3c76c73d5`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0641a69e7e1f05a1544285cb3b709a8b9228ca6d1e6d96c66a0ae3f60cbc246f`  
		Last Modified: Wed, 21 May 2025 23:38:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:284c98dff5f2a0ad150bd4211a1db129fd87428ca2dde05427a3d4470d23d784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2338855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a8b8e6552c03d26ecc498bc8ff9ea559e55ea267d60e50335e46a93423df9`

```dockerfile
```

-	Layers:
	-	`sha256:529db81d9e88463a9e87c4177e55e182fb444bfc991ca4c30bab1e9cb81936e2`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.3 MB (2313462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b94ad3350b6fceb471a3b45c6d44ab4dfbfcbe1d28aeff91254919fe0cfdc04`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 25.4 KB (25393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:949a4a30fca21f6a731aafd862d71f8b49ba9a8499f7d5fee52e7dd0cc5481c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31304875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae677ba0b021f969e80917c5866c4ad53dc0c6406cf6c32e1453b0bab9152d77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2f122115cc85d695acc4bd6bce955e259f1bbad28dc671e212eaf4793195e7`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c30cebca59bfd8fbcc77d6107f2e1f0ee44ec402a34a0a31604aa524a390a1`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.2 MB (2156961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c2d1ec6d6a0ae48f133bf8b323c42f088f609830eba9aba813c3f613ce67e5`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.3 MB (2263596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085b757a938317b0432d2c6e577bb26b74869f14bdb090efd1e3108581b8acac`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f05beedc084a77558e99193cabc217fa002c1042529df98c5208f1d819d325`  
		Last Modified: Wed, 21 May 2025 23:28:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:25e3d5e4f2c4ca9668835e3673d0f663e4034016efbd9381b33ae2b961dd7d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e5415c88643fa263a323da5616aca4b27b38aab4197943da866f83fae75f84`

```dockerfile
```

-	Layers:
	-	`sha256:acc18fbdd9cb8d010d8ea1d191203d0c8e33ba9dce4fe255c1f8419cb63173e7`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.3 MB (2308704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa9690c26e582bfe6c776880fd91701c7a69b74e44fa78dd536af4fc3e871259`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:35090b653875831ecc957a7c16c0f582c2b92090100f74ae5ca70786f2c367ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
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

### `memcached:1-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:90ff65aa470196afc5361ee16ebb344c3fb42f6317c16e4babaec1c79ad476ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5746542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c733c89a0ba90440ee956db059a3616a71a5e394c8dc9c9f6c1a9214b745d771`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3211cc8fb7612d73a250fd41e8ce1b264d4bafde9010ea586db45a946cb9dd79`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2692de63622aa06cd0ab32cbab5ebaac7c5c72f7f69c9c81711ec7196affb045`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 104.7 KB (104697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3694ff7984b804f1b2422eccdace864bc5b29564ff174a1e81f6b15ad9ad64e5`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 2.0 MB (1998247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a875c9e38db3d48eaf047d806f55e1ad705d891e17b24e691c6ae06b04416de`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d8aff7b7f4a9a5b7acb0870b99bc082dab792802823f42cb3df6bac425a03a`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:815522b8bf7a5c758712c55e2dfd2ba153f6d5def56049ebca9689c40b47036e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 KB (117423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e7d1adeedbeaad748f0fb03984aebb1f7b8d7a578733dfed68ae55a4d8aca5`

```dockerfile
```

-	Layers:
	-	`sha256:16f52c61ed51ca807453bbac564f16e1bc7438d019b75b43b432beee3917cf9e`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a618a61037789490baaad3bd81b36e771be572bc09db7bb521a4ea03c2c7199`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 23.8 KB (23790 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4d05de82436bd51ed609a745b8ddd01e296692beb5a372dcbdcf0b1f54818d03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4270486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e8bda6e6346ca01fa3a313ef7bcfcc696040d48be803f6c16922dedc8deae1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:44:25 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Dec 2020 01:44:29 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 17 Dec 2020 01:44:30 GMT
ENV MEMCACHED_VERSION=1.6.9
# Thu, 17 Dec 2020 01:44:31 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Thu, 17 Dec 2020 01:47:40 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Dec 2020 01:47:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Dec 2020 01:47:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Dec 2020 01:47:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:47:44 GMT
USER memcache
# Thu, 17 Dec 2020 01:47:45 GMT
EXPOSE 11211
# Thu, 17 Dec 2020 01:47:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc04af65958529b14246e2401008ef0186d74a33d2aa1b64d5f49633a1ff8f1`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bb28157acd02855bdf031eb7158f2cbb9849a6a9e6b45b4b82b507df6d83e9`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 14.9 KB (14904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b32778d38f805e0e2a84689dba047adda457098c6f4a0b3aeb51a9e9d3e7f2b`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 1.6 MB (1649753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506d15aa86681d1812c5696615302d2a50938410c852b6aa0d0680c7baa4589f`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55730e61cf75cdadfaf0682212c74d7a2355e652e0655cc74ba35a4b7cfb4c1`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull memcached@sha256:ac249cab7023411f8a5907f3a76e9ea920d08417bb843a490be5713136db3e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af971c76faaef52be66fc01361500e52479d9bd3de8c61e1ef111fba60d5dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f8cd16a2143448bb838f761683fc0d0414b211efd908c29739ea8fd5596ca`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ea935f106a5cac5c3db1cf082812746503193aad9a99f38a4b21f224a57e1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 120.8 KB (120773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63311bdf55b9f3cf77efa26b0da012e373d170b987229f428ce76b886bbce469`  
		Last Modified: Wed, 02 Apr 2025 00:26:44 GMT  
		Size: 2.0 MB (1989465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1d29b03fe2e901538845f42fc32d02e219b7ee32ae4e96d693d524c107f489`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bd8da7aa9a5f757c9aa94050d20b6125e7db478d3d09d066d7bacc647e82cd`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ad5f230ec532bb07cca752d58c44405687441c7cf07466de1abb8010fe83444b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 KB (117724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e862b1f07efa9790536488995533c7e658e410b55494d4f40578655c76e97e96`

```dockerfile
```

-	Layers:
	-	`sha256:2ae3d7cc25dc211d941164751cecdab1653e411fd74ac6d8792c5b3d72661cc4`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14ce594178b9c4afdf8d733cda3d894e4a9ad61c28d1ac8f7768f95d1c8f3b0b`  
		Last Modified: Wed, 02 Apr 2025 00:26:44 GMT  
		Size: 24.0 KB (23987 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:d4bdd5dcadda94a10fe78fdbf45d948bbfaa8233c6747b530c9e60319c7ba800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3154682685d8fd270595d40c1049cb408aed0282f2c747604db8442fcef5dfe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645c39e6b0ed26b821f36985348fb5422ae3b6196b7cf12ef50dda5a81d2b93`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4567ac7ea6d13e132381838b339c502058075a6fc0b18186ab1799070146919f`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 109.5 KB (109488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b78d96d6f34941f27c987768132a4c5c18ef33bd672132df7d9c5a820399226`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 2.0 MB (1959719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b507bd921881822a186cd02039a745dad142b6e8030ef7de46647172ec3830f`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5982dc98a348c1424c4189f2fc4e046ddfa92211012c880445f8c8f587fcc8`  
		Last Modified: Wed, 02 Apr 2025 00:02:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a8fcd0e85c073ee5e2cb2181ec295a8a17487566fd2c86ae081021eb5c246d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 KB (117320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b74d45db45f5c8f0ff0f375a08d4173e6d117f52c764d692162cc3c7ce2779`

```dockerfile
```

-	Layers:
	-	`sha256:200655427be8ca8fd2a9527ab234f19e1ae2927df5ae049b42f413365ecc92d9`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9ea6164d6c395a7b52b1395f9884889dd65a2f2aabf838e84561eeb87890b6c`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 23.7 KB (23732 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:846bb02f30ec4006d9b170f8e2fac3617b994e1d5ffbfcbd872c7d916523b4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022d4e1e17a86c0612d17c441ef3227d9042c46d5feecdd9c2a273b8314469e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81a068108debd592bc5100e24523483d0e5439f65b1c2eac8795522da51a6f0`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1b08fecb6beefd2da11b480a18e59255878a54a949bf6bfd470917dcafe91a`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aeecda3ee3acaf18a7673b403236cbe8d93f545f12bc55621b6f37e513900a5`  
		Last Modified: Wed, 02 Apr 2025 00:31:25 GMT  
		Size: 2.1 MB (2091349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b592e99d4871d2d634a039a4d058bed8d83febeccf5444e606b4420f0aa99c6`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c78b4428d40f07afd310ae82ed6fba84a4614528eb42ab1f92520bac7a191e0`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1656858c9dc9f1197d5b06660d09e4b57f90eed888dacf469ef312f4662e332b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 KB (115604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6a6900dce886d3fa69d25d431a1266fa1944b76e6ba8d139a5d00c0adaed75`

```dockerfile
```

-	Layers:
	-	`sha256:ec185783a159561468b1b9fadb3fd45605c017f8b76fb472b8202218447896c0`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:236149af7dac34fda2172de648c11f6afaa5c6e6566f2a909ad14f671f3c9008`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:b2d20d9478f0865295f104d69a10a6af47a42a19e0dce14f29edb38774033203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e583bfbee3cc9a94a7b502b1a173f9bf4111fca05ea1278df906891196781025`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf0ec129ec8a2b4d4a1c63ccbf427d2a09e4964506f173b2d50e16da5c5d85d`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87ff2734bb4c56d7bc73ec0ff994ec23d27330caef800d8833aabe135a40c16`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 107.9 KB (107853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efd9838e543fe84c79d3055949dc5f19a024e408550ed536f137c7c1d82dc49`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 1.9 MB (1932539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98def9beaf0eda5e2c72d1bb51c0ba6fd3c4fa353bd2ffaa71c769fc1e24e097`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ed44c8b9815cf9aebd7cb9e2526354718cbcda21e982ef1644179e23f3ed68`  
		Last Modified: Wed, 02 Apr 2025 02:42:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b79d62e7bee66523ce599bf19665532e58184f1418dcaa75319ae276df7e7102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 KB (115600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc405e5fbc58e4cbffe75922414fde14af323b70005eec6bd80a84057139b80`

```dockerfile
```

-	Layers:
	-	`sha256:f73a53dbdd9178f81244bf32411a1b2748d2a982b43a387ffa12e397da212ac3`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 91.7 KB (91736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41960c07a99d18bed2becce19308f78dbc107450842b1b59bdb2583336c463c8`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:3f70ed54bc6d6486a26fa5d844d30d158f78ee530a9b9ad92d9ee0165bbe3b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5620401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efb254b83b2d2bcf8ea4b50253aca87b5bc46f9f5593b6829b17550790a8f00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e7532ce01b9a31f1f3df73165c991b23b03e88dca43c46f5cc24237fc103d3`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff362c9247c7186b179ab36b3f74241e85aacd9e6bca6d4ef92adad9cfb9e2cd`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 113.5 KB (113461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8290f37bed0ef8feae03102a7631bc1d855099e839e088b703d3abbaf3883921`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 2.0 MB (2038025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b66de72a4b2ca75ad48d4f2e31e85116103f8e920c92abeebfcbe8a523bc048`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f9594fc6f70b3bc4eca62bf52dbc1accfd31976eef6d947935500066ec5a66`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6000519346e0e698f4e7b53de4fcdb0dc0a7295e922b1ddf5821c39083d85aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 KB (115471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c794c1f5316b791d894d4cb76365cfe77788960fbfb22ec98b8fc72b26bd0e3`

```dockerfile
```

-	Layers:
	-	`sha256:4df28bd3243c0b3247802e9fbda82c25885df47aeb6adc72737fa52615c9d38a`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbf6a1d4a771c26772accd7269d7279e63402148a1eda5a7d29db4ac1101662d`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 23.8 KB (23789 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.21`

```console
$ docker pull memcached@sha256:5ac71d3889701bd0750d35b06762ab7efc873ef29d7a43848ef5b0dc30a0dad4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
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

### `memcached:1-alpine3.21` - linux; amd64

```console
$ docker pull memcached@sha256:90ff65aa470196afc5361ee16ebb344c3fb42f6317c16e4babaec1c79ad476ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5746542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c733c89a0ba90440ee956db059a3616a71a5e394c8dc9c9f6c1a9214b745d771`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3211cc8fb7612d73a250fd41e8ce1b264d4bafde9010ea586db45a946cb9dd79`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2692de63622aa06cd0ab32cbab5ebaac7c5c72f7f69c9c81711ec7196affb045`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 104.7 KB (104697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3694ff7984b804f1b2422eccdace864bc5b29564ff174a1e81f6b15ad9ad64e5`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 2.0 MB (1998247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a875c9e38db3d48eaf047d806f55e1ad705d891e17b24e691c6ae06b04416de`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d8aff7b7f4a9a5b7acb0870b99bc082dab792802823f42cb3df6bac425a03a`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:815522b8bf7a5c758712c55e2dfd2ba153f6d5def56049ebca9689c40b47036e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 KB (117423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e7d1adeedbeaad748f0fb03984aebb1f7b8d7a578733dfed68ae55a4d8aca5`

```dockerfile
```

-	Layers:
	-	`sha256:16f52c61ed51ca807453bbac564f16e1bc7438d019b75b43b432beee3917cf9e`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a618a61037789490baaad3bd81b36e771be572bc09db7bb521a4ea03c2c7199`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 23.8 KB (23790 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ac249cab7023411f8a5907f3a76e9ea920d08417bb843a490be5713136db3e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af971c76faaef52be66fc01361500e52479d9bd3de8c61e1ef111fba60d5dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f8cd16a2143448bb838f761683fc0d0414b211efd908c29739ea8fd5596ca`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ea935f106a5cac5c3db1cf082812746503193aad9a99f38a4b21f224a57e1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 120.8 KB (120773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63311bdf55b9f3cf77efa26b0da012e373d170b987229f428ce76b886bbce469`  
		Last Modified: Wed, 02 Apr 2025 00:26:44 GMT  
		Size: 2.0 MB (1989465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1d29b03fe2e901538845f42fc32d02e219b7ee32ae4e96d693d524c107f489`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bd8da7aa9a5f757c9aa94050d20b6125e7db478d3d09d066d7bacc647e82cd`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:ad5f230ec532bb07cca752d58c44405687441c7cf07466de1abb8010fe83444b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 KB (117724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e862b1f07efa9790536488995533c7e658e410b55494d4f40578655c76e97e96`

```dockerfile
```

-	Layers:
	-	`sha256:2ae3d7cc25dc211d941164751cecdab1653e411fd74ac6d8792c5b3d72661cc4`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14ce594178b9c4afdf8d733cda3d894e4a9ad61c28d1ac8f7768f95d1c8f3b0b`  
		Last Modified: Wed, 02 Apr 2025 00:26:44 GMT  
		Size: 24.0 KB (23987 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:d4bdd5dcadda94a10fe78fdbf45d948bbfaa8233c6747b530c9e60319c7ba800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3154682685d8fd270595d40c1049cb408aed0282f2c747604db8442fcef5dfe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645c39e6b0ed26b821f36985348fb5422ae3b6196b7cf12ef50dda5a81d2b93`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4567ac7ea6d13e132381838b339c502058075a6fc0b18186ab1799070146919f`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 109.5 KB (109488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b78d96d6f34941f27c987768132a4c5c18ef33bd672132df7d9c5a820399226`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 2.0 MB (1959719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b507bd921881822a186cd02039a745dad142b6e8030ef7de46647172ec3830f`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5982dc98a348c1424c4189f2fc4e046ddfa92211012c880445f8c8f587fcc8`  
		Last Modified: Wed, 02 Apr 2025 00:02:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:a8fcd0e85c073ee5e2cb2181ec295a8a17487566fd2c86ae081021eb5c246d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 KB (117320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b74d45db45f5c8f0ff0f375a08d4173e6d117f52c764d692162cc3c7ce2779`

```dockerfile
```

-	Layers:
	-	`sha256:200655427be8ca8fd2a9527ab234f19e1ae2927df5ae049b42f413365ecc92d9`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9ea6164d6c395a7b52b1395f9884889dd65a2f2aabf838e84561eeb87890b6c`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 23.7 KB (23732 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:846bb02f30ec4006d9b170f8e2fac3617b994e1d5ffbfcbd872c7d916523b4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022d4e1e17a86c0612d17c441ef3227d9042c46d5feecdd9c2a273b8314469e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81a068108debd592bc5100e24523483d0e5439f65b1c2eac8795522da51a6f0`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1b08fecb6beefd2da11b480a18e59255878a54a949bf6bfd470917dcafe91a`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aeecda3ee3acaf18a7673b403236cbe8d93f545f12bc55621b6f37e513900a5`  
		Last Modified: Wed, 02 Apr 2025 00:31:25 GMT  
		Size: 2.1 MB (2091349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b592e99d4871d2d634a039a4d058bed8d83febeccf5444e606b4420f0aa99c6`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c78b4428d40f07afd310ae82ed6fba84a4614528eb42ab1f92520bac7a191e0`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:1656858c9dc9f1197d5b06660d09e4b57f90eed888dacf469ef312f4662e332b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 KB (115604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6a6900dce886d3fa69d25d431a1266fa1944b76e6ba8d139a5d00c0adaed75`

```dockerfile
```

-	Layers:
	-	`sha256:ec185783a159561468b1b9fadb3fd45605c017f8b76fb472b8202218447896c0`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:236149af7dac34fda2172de648c11f6afaa5c6e6566f2a909ad14f671f3c9008`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; riscv64

```console
$ docker pull memcached@sha256:b2d20d9478f0865295f104d69a10a6af47a42a19e0dce14f29edb38774033203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e583bfbee3cc9a94a7b502b1a173f9bf4111fca05ea1278df906891196781025`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf0ec129ec8a2b4d4a1c63ccbf427d2a09e4964506f173b2d50e16da5c5d85d`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87ff2734bb4c56d7bc73ec0ff994ec23d27330caef800d8833aabe135a40c16`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 107.9 KB (107853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efd9838e543fe84c79d3055949dc5f19a024e408550ed536f137c7c1d82dc49`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 1.9 MB (1932539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98def9beaf0eda5e2c72d1bb51c0ba6fd3c4fa353bd2ffaa71c769fc1e24e097`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ed44c8b9815cf9aebd7cb9e2526354718cbcda21e982ef1644179e23f3ed68`  
		Last Modified: Wed, 02 Apr 2025 02:42:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:b79d62e7bee66523ce599bf19665532e58184f1418dcaa75319ae276df7e7102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 KB (115600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc405e5fbc58e4cbffe75922414fde14af323b70005eec6bd80a84057139b80`

```dockerfile
```

-	Layers:
	-	`sha256:f73a53dbdd9178f81244bf32411a1b2748d2a982b43a387ffa12e397da212ac3`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 91.7 KB (91736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41960c07a99d18bed2becce19308f78dbc107450842b1b59bdb2583336c463c8`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:3f70ed54bc6d6486a26fa5d844d30d158f78ee530a9b9ad92d9ee0165bbe3b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5620401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efb254b83b2d2bcf8ea4b50253aca87b5bc46f9f5593b6829b17550790a8f00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e7532ce01b9a31f1f3df73165c991b23b03e88dca43c46f5cc24237fc103d3`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff362c9247c7186b179ab36b3f74241e85aacd9e6bca6d4ef92adad9cfb9e2cd`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 113.5 KB (113461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8290f37bed0ef8feae03102a7631bc1d855099e839e088b703d3abbaf3883921`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 2.0 MB (2038025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b66de72a4b2ca75ad48d4f2e31e85116103f8e920c92abeebfcbe8a523bc048`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f9594fc6f70b3bc4eca62bf52dbc1accfd31976eef6d947935500066ec5a66`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:6000519346e0e698f4e7b53de4fcdb0dc0a7295e922b1ddf5821c39083d85aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 KB (115471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c794c1f5316b791d894d4cb76365cfe77788960fbfb22ec98b8fc72b26bd0e3`

```dockerfile
```

-	Layers:
	-	`sha256:4df28bd3243c0b3247802e9fbda82c25885df47aeb6adc72737fa52615c9d38a`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbf6a1d4a771c26772accd7269d7279e63402148a1eda5a7d29db4ac1101662d`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 23.8 KB (23789 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:0f92cdf1ca059c3b747f95328ed9e8de40866896657cb2b73148be36331efc02
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

### `memcached:1-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:15c127398e9bb6bdfdbd6689b817964617401f2d9ca294758323011b3bb09350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33021901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f40f7fb4f0d5e586a146a0a994596292ea1e784ca1657eed1192b2fe17a003c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62639a9e53d980a0e86e3b54ae34e1e913a7f6cebd1bce7741e629047b732896`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5783d9aa8a04d558f9d1d5407d3f6dddb064b0a670738a5cbc480866bbc1a30`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.5 MB (2492219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609bfa774ee059a5d07cc14920af077ac7de9039c567f38164ea31f5eb04d3ba`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.3 MB (2302838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062ee789e2fd31345a9db851ddb0616c67ac7a4ea84e3a0e953af88faa98e3e5`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8416b27aabc571df320856a2ff533825bcbfc2fa602782561ff6b1a0449b821`  
		Last Modified: Wed, 21 May 2025 23:16:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7b5eaaa81772b0dc7377f0c8a8d41bb09c38c1a07292c0e0bef5654ceef3a28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c8287d2eb936f10093c74288a99d09a35c07df6033435ba68847dba2b0fdff`

```dockerfile
```

-	Layers:
	-	`sha256:f5c222a0451ee4a8115a7a9421176131c1481dd511e4ec028e050fdf94e7b741`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.3 MB (2308990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01ac10f70adef13c64045d3be5956b00caafe800e1fab7640f6eaa5f9ea66864`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:9d0d272209b7fd9922e4184de83ab429d527ad56c2f92a6a262cb88cf331551e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30087755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8113ec8739204304b1054312c93717e8c84189d23a003648ffa966d472462cad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01741d1d3bd96678d0f5dccb883892b5af0a3ffb6fe1abaf71cfa8d27579819`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e33674278ab7a59427b75a5c5a4fc74379bdc2cea1105e212becedfd13aadc`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.1 MB (2097064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c00b2be2834a255d33718d0903d2637ed005c981ee3d72a52654f7e0aed5e78`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.2 MB (2232281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148a70549f08f93b07f1c60ad72af807c88405d06687d9fe374648b9a484d40e`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93adc89552cc46d51abc366499a6fac900badfa05b8a0c8c604a7e4ac0cae40`  
		Last Modified: Wed, 21 May 2025 23:46:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7659c54d461b01b9e2062f0a8843b75b7d6a793c3d358a339b78e071770dcbd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2338302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af770cd911aab0856b542fdf7bc835ddf01b1ce26aa176b7b9cacfbc9388fb2d`

```dockerfile
```

-	Layers:
	-	`sha256:6d50a9e0dd879a75ce6c9396bd03c5ecb9beefd32a2d5bd6cf54f36341327685`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.3 MB (2312836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f3107fa09f2c0b66f32bebd5a1bb01208c84b9fa1da768bf5a5dbd20ca500d0`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v7

```console
$ docker pull memcached@sha256:95630a66e2d5c3a453ccc0f22d18ce0a297f1f21536938ff8f1b93c86b9cfbea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28065225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127e001dab188acb98ae7340be866c4c3ae686a9285cf40bd10f9dc702a73ee9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b5a50ba24d961f5862446c5e48fe0c5dbf9acfb0a3718255dd76fab71e84a7`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4adc063a4b96db7c50bcc78cd236a7102a3c31a61fb4216967b2cdcab50c24`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 1.9 MB (1946317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26fc15d35761b3f0c7797ea1ffc39ab51d4227089df7d6b5d2a075730795d20`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 2.2 MB (2184474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64f51527fd9673b0b39f52e4d608185f9461b4282e581e5ef1ce245bdc451e8`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138b4847c3beba31cf3c1807f17ce0b970ec15f04604f92ac076ff994c1a0f68`  
		Last Modified: Wed, 21 May 2025 23:49:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2f6b92592e3f57dbba3221b48b0dce566be344c3e646a89421cfc68ac2827925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857e0ef0a015c3e4c292fe0a24e960bbfba6c8f5844e8022a8d5c11a52d798c8`

```dockerfile
```

-	Layers:
	-	`sha256:7fb0e5e8b1ea53e4ba20b1cee752d37de3b49eaa2c057aea103fb67ad94a2cf5`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 2.3 MB (2311273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:210181bb919654e239b27e79e0a1003bde8ec7d3dd27841dfb0f95d0c62d23d4`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4fc35e2dfad1e5506199e79f54d5400afd22aee2bb1fe0b5e554d051c7c38d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32711358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d9217ce2913b829164781088c527a86fb1d43a48403bfd92c09a9ce7fd4c95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661e0135b0352aad675030e66bdddcf402a36cea02deb2532b0a24d5ba27554`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e7084e0aea669193e1cab086c096bd0764a05f1bf138e1f7c8f0c04eaf3b52`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.4 MB (2355810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259807b0c15878094bf0f3b13afedc0ef32d7eb679af66072ae18096127d72e1`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.3 MB (2288755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacab3ed6c99f53a622eefcda0dee8f57e377bfb97e7f57674e5030b7172988c`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12316079cc5378e29c63fc769e3686207ce41caec7ed76e8e5bb2c3e3b9a4938`  
		Last Modified: Thu, 22 May 2025 00:10:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:ed76bdc15573ee04e086b0a05bfe7056bb260ef0625d8fca2b4c89bd490db508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282362d3d316c5b5bd6b78ff5cfdd9be97d18c3c0018244eeac32f5a123b7d24`

```dockerfile
```

-	Layers:
	-	`sha256:f50a38ae76734a0eff8b24f4e99acd0d1bdb9ab848e04f9ddbcdcf08aadbe908`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.3 MB (2309305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ec44f0bfbd8d8065048e9d7bc8c90c0dcc460586efa613acacb43cb444f3c91`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 25.5 KB (25516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:427a7ad7f639e7cbf4161751cad9450044cbfaf6be8180abc51e01f68cad186c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33962949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a7e05a07d6b637c8752b13cee1ed7a5ebe2a4ef846c0eecaf4b7904d07ff4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d0594fdf9f07f23d90458a489d7972ab011bc5cca342af82850c3e9c024e3e`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4797e4e934c0c059a34c8b9d6c2adc40dece3f2ba61185edfa1c36591ef3549f`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.5 MB (2502658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7cc241a1440cfefd9f5b88cb6233b9ee820398da0c74155859c3114dd0646c`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.3 MB (2251292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cacd3ce01b0221992568e7179a1408774519b7dfbfc1daf37095764ae9bf16`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4abb18b4fabd731df2a3dbba62cd3f6de6cc4a6ab8419827bcbeb87641c4ad7`  
		Last Modified: Wed, 21 May 2025 23:16:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3c7de609f262a2ab1ddafedf272ac08f1eded0a2b08450f76dbd927b4b746f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfd69fc1ff5ceb8e449d8374c86427aafe41200a46c937aee60fce7a21ebf13`

```dockerfile
```

-	Layers:
	-	`sha256:87803ae24543fc1d1ecf0d1af68207e9714fd56829bab2354f9dd3940e3cf240`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.3 MB (2306133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b6feaf94b04b7737bdbf12b7c3f15ea0f7c46ead6614b9a46a82b87b5e5c75`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:55e7557e19928aa1991fbb59dcb75ea75b5b87115b772f36fd7302618c031468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32774540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1d55a83743e8701a5f0aacd60bd4260744537318e9335e6f681f765a2f536e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Wed, 21 May 2025 22:28:22 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00be87e076613598c61cb34d1eab1a04e74cb16c312c6b2737aaa5b2f54f0cad`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4fdba1c45e7b51399330c05d6b7e619f96cc0ed80cfd6bc75722cf5c982105`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 1.9 MB (1944079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d0d8b3f93dba36eb05fef21a3cda9faaf4e064e161fb87965839f9da4a2a20`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 2.3 MB (2317092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d4a6285da352b0857160c9194204e6801269736b4b18ca39bead26e9be8345`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d044aab1c575f4ebf7752dd0c9d988fc02e7b6f86316622b1678cea3cb9ca44`  
		Last Modified: Thu, 22 May 2025 00:11:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:048fdf15ee7c39e63ec03618e8587191e3915649f1b0076574f19773f9ccf067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c546fba658eb64c00d4036d1ac6c25e4a6f0b1681950c03a94ffc3954fb0d5c9`

```dockerfile
```

-	Layers:
	-	`sha256:2d39a6be744c7e579e7d4147fdc82a19956c6223fcb98601955e9a0a5d1e9e2e`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 25.2 KB (25216 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:3e871b866378795839b5bac555437a97646aa6f1c2abccdd182fe6b8ea84c983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37197690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9129b120bccf4a13f93ae0e47a4046e9ab94b4ff2d8de473eb248683b2802a6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Wed, 21 May 2025 22:28:16 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50fa062d3f9b2ead925a10e36e54327c0aae0c280d34e1075bcf82708310f13`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c345e70ea367cfeb023138dcae0d694e941f247957111430bd191f08181ef2b`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.7 MB (2710200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bd27f00915f27350ad09f9ca295e22cc787fe09c28db9040ad1bfcbfb1508d`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.4 MB (2419066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eee08866234c70e5aa7c719d396e45b9f8955b9a790d0654fd365d3c76c73d5`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0641a69e7e1f05a1544285cb3b709a8b9228ca6d1e6d96c66a0ae3f60cbc246f`  
		Last Modified: Wed, 21 May 2025 23:38:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:284c98dff5f2a0ad150bd4211a1db129fd87428ca2dde05427a3d4470d23d784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2338855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a8b8e6552c03d26ecc498bc8ff9ea559e55ea267d60e50335e46a93423df9`

```dockerfile
```

-	Layers:
	-	`sha256:529db81d9e88463a9e87c4177e55e182fb444bfc991ca4c30bab1e9cb81936e2`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.3 MB (2313462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b94ad3350b6fceb471a3b45c6d44ab4dfbfcbe1d28aeff91254919fe0cfdc04`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 25.4 KB (25393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:949a4a30fca21f6a731aafd862d71f8b49ba9a8499f7d5fee52e7dd0cc5481c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31304875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae677ba0b021f969e80917c5866c4ad53dc0c6406cf6c32e1453b0bab9152d77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2f122115cc85d695acc4bd6bce955e259f1bbad28dc671e212eaf4793195e7`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c30cebca59bfd8fbcc77d6107f2e1f0ee44ec402a34a0a31604aa524a390a1`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.2 MB (2156961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c2d1ec6d6a0ae48f133bf8b323c42f088f609830eba9aba813c3f613ce67e5`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.3 MB (2263596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085b757a938317b0432d2c6e577bb26b74869f14bdb090efd1e3108581b8acac`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f05beedc084a77558e99193cabc217fa002c1042529df98c5208f1d819d325`  
		Last Modified: Wed, 21 May 2025 23:28:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:25e3d5e4f2c4ca9668835e3673d0f663e4034016efbd9381b33ae2b961dd7d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e5415c88643fa263a323da5616aca4b27b38aab4197943da866f83fae75f84`

```dockerfile
```

-	Layers:
	-	`sha256:acc18fbdd9cb8d010d8ea1d191203d0c8e33ba9dce4fe255c1f8419cb63173e7`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.3 MB (2308704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa9690c26e582bfe6c776880fd91701c7a69b74e44fa78dd536af4fc3e871259`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:0f92cdf1ca059c3b747f95328ed9e8de40866896657cb2b73148be36331efc02
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

### `memcached:1.6` - linux; amd64

```console
$ docker pull memcached@sha256:15c127398e9bb6bdfdbd6689b817964617401f2d9ca294758323011b3bb09350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33021901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f40f7fb4f0d5e586a146a0a994596292ea1e784ca1657eed1192b2fe17a003c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62639a9e53d980a0e86e3b54ae34e1e913a7f6cebd1bce7741e629047b732896`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5783d9aa8a04d558f9d1d5407d3f6dddb064b0a670738a5cbc480866bbc1a30`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.5 MB (2492219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609bfa774ee059a5d07cc14920af077ac7de9039c567f38164ea31f5eb04d3ba`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.3 MB (2302838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062ee789e2fd31345a9db851ddb0616c67ac7a4ea84e3a0e953af88faa98e3e5`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8416b27aabc571df320856a2ff533825bcbfc2fa602782561ff6b1a0449b821`  
		Last Modified: Wed, 21 May 2025 23:16:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:7b5eaaa81772b0dc7377f0c8a8d41bb09c38c1a07292c0e0bef5654ceef3a28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c8287d2eb936f10093c74288a99d09a35c07df6033435ba68847dba2b0fdff`

```dockerfile
```

-	Layers:
	-	`sha256:f5c222a0451ee4a8115a7a9421176131c1481dd511e4ec028e050fdf94e7b741`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.3 MB (2308990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01ac10f70adef13c64045d3be5956b00caafe800e1fab7640f6eaa5f9ea66864`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:9d0d272209b7fd9922e4184de83ab429d527ad56c2f92a6a262cb88cf331551e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30087755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8113ec8739204304b1054312c93717e8c84189d23a003648ffa966d472462cad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01741d1d3bd96678d0f5dccb883892b5af0a3ffb6fe1abaf71cfa8d27579819`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e33674278ab7a59427b75a5c5a4fc74379bdc2cea1105e212becedfd13aadc`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.1 MB (2097064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c00b2be2834a255d33718d0903d2637ed005c981ee3d72a52654f7e0aed5e78`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.2 MB (2232281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148a70549f08f93b07f1c60ad72af807c88405d06687d9fe374648b9a484d40e`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93adc89552cc46d51abc366499a6fac900badfa05b8a0c8c604a7e4ac0cae40`  
		Last Modified: Wed, 21 May 2025 23:46:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:7659c54d461b01b9e2062f0a8843b75b7d6a793c3d358a339b78e071770dcbd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2338302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af770cd911aab0856b542fdf7bc835ddf01b1ce26aa176b7b9cacfbc9388fb2d`

```dockerfile
```

-	Layers:
	-	`sha256:6d50a9e0dd879a75ce6c9396bd03c5ecb9beefd32a2d5bd6cf54f36341327685`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.3 MB (2312836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f3107fa09f2c0b66f32bebd5a1bb01208c84b9fa1da768bf5a5dbd20ca500d0`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:95630a66e2d5c3a453ccc0f22d18ce0a297f1f21536938ff8f1b93c86b9cfbea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28065225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127e001dab188acb98ae7340be866c4c3ae686a9285cf40bd10f9dc702a73ee9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b5a50ba24d961f5862446c5e48fe0c5dbf9acfb0a3718255dd76fab71e84a7`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4adc063a4b96db7c50bcc78cd236a7102a3c31a61fb4216967b2cdcab50c24`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 1.9 MB (1946317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26fc15d35761b3f0c7797ea1ffc39ab51d4227089df7d6b5d2a075730795d20`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 2.2 MB (2184474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64f51527fd9673b0b39f52e4d608185f9461b4282e581e5ef1ce245bdc451e8`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138b4847c3beba31cf3c1807f17ce0b970ec15f04604f92ac076ff994c1a0f68`  
		Last Modified: Wed, 21 May 2025 23:49:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:2f6b92592e3f57dbba3221b48b0dce566be344c3e646a89421cfc68ac2827925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857e0ef0a015c3e4c292fe0a24e960bbfba6c8f5844e8022a8d5c11a52d798c8`

```dockerfile
```

-	Layers:
	-	`sha256:7fb0e5e8b1ea53e4ba20b1cee752d37de3b49eaa2c057aea103fb67ad94a2cf5`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 2.3 MB (2311273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:210181bb919654e239b27e79e0a1003bde8ec7d3dd27841dfb0f95d0c62d23d4`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4fc35e2dfad1e5506199e79f54d5400afd22aee2bb1fe0b5e554d051c7c38d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32711358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d9217ce2913b829164781088c527a86fb1d43a48403bfd92c09a9ce7fd4c95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661e0135b0352aad675030e66bdddcf402a36cea02deb2532b0a24d5ba27554`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e7084e0aea669193e1cab086c096bd0764a05f1bf138e1f7c8f0c04eaf3b52`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.4 MB (2355810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259807b0c15878094bf0f3b13afedc0ef32d7eb679af66072ae18096127d72e1`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.3 MB (2288755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacab3ed6c99f53a622eefcda0dee8f57e377bfb97e7f57674e5030b7172988c`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12316079cc5378e29c63fc769e3686207ce41caec7ed76e8e5bb2c3e3b9a4938`  
		Last Modified: Thu, 22 May 2025 00:10:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:ed76bdc15573ee04e086b0a05bfe7056bb260ef0625d8fca2b4c89bd490db508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282362d3d316c5b5bd6b78ff5cfdd9be97d18c3c0018244eeac32f5a123b7d24`

```dockerfile
```

-	Layers:
	-	`sha256:f50a38ae76734a0eff8b24f4e99acd0d1bdb9ab848e04f9ddbcdcf08aadbe908`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.3 MB (2309305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ec44f0bfbd8d8065048e9d7bc8c90c0dcc460586efa613acacb43cb444f3c91`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 25.5 KB (25516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:427a7ad7f639e7cbf4161751cad9450044cbfaf6be8180abc51e01f68cad186c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33962949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a7e05a07d6b637c8752b13cee1ed7a5ebe2a4ef846c0eecaf4b7904d07ff4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d0594fdf9f07f23d90458a489d7972ab011bc5cca342af82850c3e9c024e3e`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4797e4e934c0c059a34c8b9d6c2adc40dece3f2ba61185edfa1c36591ef3549f`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.5 MB (2502658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7cc241a1440cfefd9f5b88cb6233b9ee820398da0c74155859c3114dd0646c`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.3 MB (2251292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cacd3ce01b0221992568e7179a1408774519b7dfbfc1daf37095764ae9bf16`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4abb18b4fabd731df2a3dbba62cd3f6de6cc4a6ab8419827bcbeb87641c4ad7`  
		Last Modified: Wed, 21 May 2025 23:16:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:3c7de609f262a2ab1ddafedf272ac08f1eded0a2b08450f76dbd927b4b746f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfd69fc1ff5ceb8e449d8374c86427aafe41200a46c937aee60fce7a21ebf13`

```dockerfile
```

-	Layers:
	-	`sha256:87803ae24543fc1d1ecf0d1af68207e9714fd56829bab2354f9dd3940e3cf240`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.3 MB (2306133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b6feaf94b04b7737bdbf12b7c3f15ea0f7c46ead6614b9a46a82b87b5e5c75`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:55e7557e19928aa1991fbb59dcb75ea75b5b87115b772f36fd7302618c031468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32774540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1d55a83743e8701a5f0aacd60bd4260744537318e9335e6f681f765a2f536e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Wed, 21 May 2025 22:28:22 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00be87e076613598c61cb34d1eab1a04e74cb16c312c6b2737aaa5b2f54f0cad`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4fdba1c45e7b51399330c05d6b7e619f96cc0ed80cfd6bc75722cf5c982105`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 1.9 MB (1944079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d0d8b3f93dba36eb05fef21a3cda9faaf4e064e161fb87965839f9da4a2a20`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 2.3 MB (2317092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d4a6285da352b0857160c9194204e6801269736b4b18ca39bead26e9be8345`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d044aab1c575f4ebf7752dd0c9d988fc02e7b6f86316622b1678cea3cb9ca44`  
		Last Modified: Thu, 22 May 2025 00:11:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:048fdf15ee7c39e63ec03618e8587191e3915649f1b0076574f19773f9ccf067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c546fba658eb64c00d4036d1ac6c25e4a6f0b1681950c03a94ffc3954fb0d5c9`

```dockerfile
```

-	Layers:
	-	`sha256:2d39a6be744c7e579e7d4147fdc82a19956c6223fcb98601955e9a0a5d1e9e2e`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 25.2 KB (25216 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:3e871b866378795839b5bac555437a97646aa6f1c2abccdd182fe6b8ea84c983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37197690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9129b120bccf4a13f93ae0e47a4046e9ab94b4ff2d8de473eb248683b2802a6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Wed, 21 May 2025 22:28:16 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50fa062d3f9b2ead925a10e36e54327c0aae0c280d34e1075bcf82708310f13`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c345e70ea367cfeb023138dcae0d694e941f247957111430bd191f08181ef2b`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.7 MB (2710200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bd27f00915f27350ad09f9ca295e22cc787fe09c28db9040ad1bfcbfb1508d`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.4 MB (2419066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eee08866234c70e5aa7c719d396e45b9f8955b9a790d0654fd365d3c76c73d5`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0641a69e7e1f05a1544285cb3b709a8b9228ca6d1e6d96c66a0ae3f60cbc246f`  
		Last Modified: Wed, 21 May 2025 23:38:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:284c98dff5f2a0ad150bd4211a1db129fd87428ca2dde05427a3d4470d23d784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2338855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a8b8e6552c03d26ecc498bc8ff9ea559e55ea267d60e50335e46a93423df9`

```dockerfile
```

-	Layers:
	-	`sha256:529db81d9e88463a9e87c4177e55e182fb444bfc991ca4c30bab1e9cb81936e2`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.3 MB (2313462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b94ad3350b6fceb471a3b45c6d44ab4dfbfcbe1d28aeff91254919fe0cfdc04`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 25.4 KB (25393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:949a4a30fca21f6a731aafd862d71f8b49ba9a8499f7d5fee52e7dd0cc5481c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31304875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae677ba0b021f969e80917c5866c4ad53dc0c6406cf6c32e1453b0bab9152d77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2f122115cc85d695acc4bd6bce955e259f1bbad28dc671e212eaf4793195e7`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c30cebca59bfd8fbcc77d6107f2e1f0ee44ec402a34a0a31604aa524a390a1`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.2 MB (2156961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c2d1ec6d6a0ae48f133bf8b323c42f088f609830eba9aba813c3f613ce67e5`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.3 MB (2263596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085b757a938317b0432d2c6e577bb26b74869f14bdb090efd1e3108581b8acac`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f05beedc084a77558e99193cabc217fa002c1042529df98c5208f1d819d325`  
		Last Modified: Wed, 21 May 2025 23:28:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:25e3d5e4f2c4ca9668835e3673d0f663e4034016efbd9381b33ae2b961dd7d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e5415c88643fa263a323da5616aca4b27b38aab4197943da866f83fae75f84`

```dockerfile
```

-	Layers:
	-	`sha256:acc18fbdd9cb8d010d8ea1d191203d0c8e33ba9dce4fe255c1f8419cb63173e7`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.3 MB (2308704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa9690c26e582bfe6c776880fd91701c7a69b74e44fa78dd536af4fc3e871259`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:35090b653875831ecc957a7c16c0f582c2b92090100f74ae5ca70786f2c367ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
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

### `memcached:1.6-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:90ff65aa470196afc5361ee16ebb344c3fb42f6317c16e4babaec1c79ad476ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5746542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c733c89a0ba90440ee956db059a3616a71a5e394c8dc9c9f6c1a9214b745d771`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3211cc8fb7612d73a250fd41e8ce1b264d4bafde9010ea586db45a946cb9dd79`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2692de63622aa06cd0ab32cbab5ebaac7c5c72f7f69c9c81711ec7196affb045`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 104.7 KB (104697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3694ff7984b804f1b2422eccdace864bc5b29564ff174a1e81f6b15ad9ad64e5`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 2.0 MB (1998247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a875c9e38db3d48eaf047d806f55e1ad705d891e17b24e691c6ae06b04416de`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d8aff7b7f4a9a5b7acb0870b99bc082dab792802823f42cb3df6bac425a03a`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:815522b8bf7a5c758712c55e2dfd2ba153f6d5def56049ebca9689c40b47036e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 KB (117423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e7d1adeedbeaad748f0fb03984aebb1f7b8d7a578733dfed68ae55a4d8aca5`

```dockerfile
```

-	Layers:
	-	`sha256:16f52c61ed51ca807453bbac564f16e1bc7438d019b75b43b432beee3917cf9e`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a618a61037789490baaad3bd81b36e771be572bc09db7bb521a4ea03c2c7199`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 23.8 KB (23790 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4d05de82436bd51ed609a745b8ddd01e296692beb5a372dcbdcf0b1f54818d03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4270486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e8bda6e6346ca01fa3a313ef7bcfcc696040d48be803f6c16922dedc8deae1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:44:25 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Dec 2020 01:44:29 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 17 Dec 2020 01:44:30 GMT
ENV MEMCACHED_VERSION=1.6.9
# Thu, 17 Dec 2020 01:44:31 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Thu, 17 Dec 2020 01:47:40 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Dec 2020 01:47:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Dec 2020 01:47:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Dec 2020 01:47:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:47:44 GMT
USER memcache
# Thu, 17 Dec 2020 01:47:45 GMT
EXPOSE 11211
# Thu, 17 Dec 2020 01:47:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc04af65958529b14246e2401008ef0186d74a33d2aa1b64d5f49633a1ff8f1`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bb28157acd02855bdf031eb7158f2cbb9849a6a9e6b45b4b82b507df6d83e9`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 14.9 KB (14904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b32778d38f805e0e2a84689dba047adda457098c6f4a0b3aeb51a9e9d3e7f2b`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 1.6 MB (1649753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506d15aa86681d1812c5696615302d2a50938410c852b6aa0d0680c7baa4589f`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55730e61cf75cdadfaf0682212c74d7a2355e652e0655cc74ba35a4b7cfb4c1`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull memcached@sha256:ac249cab7023411f8a5907f3a76e9ea920d08417bb843a490be5713136db3e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af971c76faaef52be66fc01361500e52479d9bd3de8c61e1ef111fba60d5dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f8cd16a2143448bb838f761683fc0d0414b211efd908c29739ea8fd5596ca`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ea935f106a5cac5c3db1cf082812746503193aad9a99f38a4b21f224a57e1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 120.8 KB (120773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63311bdf55b9f3cf77efa26b0da012e373d170b987229f428ce76b886bbce469`  
		Last Modified: Wed, 02 Apr 2025 00:26:44 GMT  
		Size: 2.0 MB (1989465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1d29b03fe2e901538845f42fc32d02e219b7ee32ae4e96d693d524c107f489`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bd8da7aa9a5f757c9aa94050d20b6125e7db478d3d09d066d7bacc647e82cd`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ad5f230ec532bb07cca752d58c44405687441c7cf07466de1abb8010fe83444b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 KB (117724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e862b1f07efa9790536488995533c7e658e410b55494d4f40578655c76e97e96`

```dockerfile
```

-	Layers:
	-	`sha256:2ae3d7cc25dc211d941164751cecdab1653e411fd74ac6d8792c5b3d72661cc4`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14ce594178b9c4afdf8d733cda3d894e4a9ad61c28d1ac8f7768f95d1c8f3b0b`  
		Last Modified: Wed, 02 Apr 2025 00:26:44 GMT  
		Size: 24.0 KB (23987 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:d4bdd5dcadda94a10fe78fdbf45d948bbfaa8233c6747b530c9e60319c7ba800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3154682685d8fd270595d40c1049cb408aed0282f2c747604db8442fcef5dfe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645c39e6b0ed26b821f36985348fb5422ae3b6196b7cf12ef50dda5a81d2b93`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4567ac7ea6d13e132381838b339c502058075a6fc0b18186ab1799070146919f`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 109.5 KB (109488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b78d96d6f34941f27c987768132a4c5c18ef33bd672132df7d9c5a820399226`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 2.0 MB (1959719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b507bd921881822a186cd02039a745dad142b6e8030ef7de46647172ec3830f`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5982dc98a348c1424c4189f2fc4e046ddfa92211012c880445f8c8f587fcc8`  
		Last Modified: Wed, 02 Apr 2025 00:02:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a8fcd0e85c073ee5e2cb2181ec295a8a17487566fd2c86ae081021eb5c246d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 KB (117320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b74d45db45f5c8f0ff0f375a08d4173e6d117f52c764d692162cc3c7ce2779`

```dockerfile
```

-	Layers:
	-	`sha256:200655427be8ca8fd2a9527ab234f19e1ae2927df5ae049b42f413365ecc92d9`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9ea6164d6c395a7b52b1395f9884889dd65a2f2aabf838e84561eeb87890b6c`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 23.7 KB (23732 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:846bb02f30ec4006d9b170f8e2fac3617b994e1d5ffbfcbd872c7d916523b4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022d4e1e17a86c0612d17c441ef3227d9042c46d5feecdd9c2a273b8314469e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81a068108debd592bc5100e24523483d0e5439f65b1c2eac8795522da51a6f0`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1b08fecb6beefd2da11b480a18e59255878a54a949bf6bfd470917dcafe91a`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aeecda3ee3acaf18a7673b403236cbe8d93f545f12bc55621b6f37e513900a5`  
		Last Modified: Wed, 02 Apr 2025 00:31:25 GMT  
		Size: 2.1 MB (2091349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b592e99d4871d2d634a039a4d058bed8d83febeccf5444e606b4420f0aa99c6`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c78b4428d40f07afd310ae82ed6fba84a4614528eb42ab1f92520bac7a191e0`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1656858c9dc9f1197d5b06660d09e4b57f90eed888dacf469ef312f4662e332b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 KB (115604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6a6900dce886d3fa69d25d431a1266fa1944b76e6ba8d139a5d00c0adaed75`

```dockerfile
```

-	Layers:
	-	`sha256:ec185783a159561468b1b9fadb3fd45605c017f8b76fb472b8202218447896c0`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:236149af7dac34fda2172de648c11f6afaa5c6e6566f2a909ad14f671f3c9008`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:b2d20d9478f0865295f104d69a10a6af47a42a19e0dce14f29edb38774033203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e583bfbee3cc9a94a7b502b1a173f9bf4111fca05ea1278df906891196781025`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf0ec129ec8a2b4d4a1c63ccbf427d2a09e4964506f173b2d50e16da5c5d85d`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87ff2734bb4c56d7bc73ec0ff994ec23d27330caef800d8833aabe135a40c16`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 107.9 KB (107853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efd9838e543fe84c79d3055949dc5f19a024e408550ed536f137c7c1d82dc49`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 1.9 MB (1932539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98def9beaf0eda5e2c72d1bb51c0ba6fd3c4fa353bd2ffaa71c769fc1e24e097`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ed44c8b9815cf9aebd7cb9e2526354718cbcda21e982ef1644179e23f3ed68`  
		Last Modified: Wed, 02 Apr 2025 02:42:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b79d62e7bee66523ce599bf19665532e58184f1418dcaa75319ae276df7e7102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 KB (115600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc405e5fbc58e4cbffe75922414fde14af323b70005eec6bd80a84057139b80`

```dockerfile
```

-	Layers:
	-	`sha256:f73a53dbdd9178f81244bf32411a1b2748d2a982b43a387ffa12e397da212ac3`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 91.7 KB (91736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41960c07a99d18bed2becce19308f78dbc107450842b1b59bdb2583336c463c8`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:3f70ed54bc6d6486a26fa5d844d30d158f78ee530a9b9ad92d9ee0165bbe3b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5620401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efb254b83b2d2bcf8ea4b50253aca87b5bc46f9f5593b6829b17550790a8f00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e7532ce01b9a31f1f3df73165c991b23b03e88dca43c46f5cc24237fc103d3`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff362c9247c7186b179ab36b3f74241e85aacd9e6bca6d4ef92adad9cfb9e2cd`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 113.5 KB (113461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8290f37bed0ef8feae03102a7631bc1d855099e839e088b703d3abbaf3883921`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 2.0 MB (2038025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b66de72a4b2ca75ad48d4f2e31e85116103f8e920c92abeebfcbe8a523bc048`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f9594fc6f70b3bc4eca62bf52dbc1accfd31976eef6d947935500066ec5a66`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6000519346e0e698f4e7b53de4fcdb0dc0a7295e922b1ddf5821c39083d85aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 KB (115471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c794c1f5316b791d894d4cb76365cfe77788960fbfb22ec98b8fc72b26bd0e3`

```dockerfile
```

-	Layers:
	-	`sha256:4df28bd3243c0b3247802e9fbda82c25885df47aeb6adc72737fa52615c9d38a`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbf6a1d4a771c26772accd7269d7279e63402148a1eda5a7d29db4ac1101662d`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 23.8 KB (23789 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.21`

```console
$ docker pull memcached@sha256:5ac71d3889701bd0750d35b06762ab7efc873ef29d7a43848ef5b0dc30a0dad4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
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

### `memcached:1.6-alpine3.21` - linux; amd64

```console
$ docker pull memcached@sha256:90ff65aa470196afc5361ee16ebb344c3fb42f6317c16e4babaec1c79ad476ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5746542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c733c89a0ba90440ee956db059a3616a71a5e394c8dc9c9f6c1a9214b745d771`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3211cc8fb7612d73a250fd41e8ce1b264d4bafde9010ea586db45a946cb9dd79`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2692de63622aa06cd0ab32cbab5ebaac7c5c72f7f69c9c81711ec7196affb045`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 104.7 KB (104697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3694ff7984b804f1b2422eccdace864bc5b29564ff174a1e81f6b15ad9ad64e5`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 2.0 MB (1998247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a875c9e38db3d48eaf047d806f55e1ad705d891e17b24e691c6ae06b04416de`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d8aff7b7f4a9a5b7acb0870b99bc082dab792802823f42cb3df6bac425a03a`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:815522b8bf7a5c758712c55e2dfd2ba153f6d5def56049ebca9689c40b47036e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 KB (117423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e7d1adeedbeaad748f0fb03984aebb1f7b8d7a578733dfed68ae55a4d8aca5`

```dockerfile
```

-	Layers:
	-	`sha256:16f52c61ed51ca807453bbac564f16e1bc7438d019b75b43b432beee3917cf9e`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a618a61037789490baaad3bd81b36e771be572bc09db7bb521a4ea03c2c7199`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 23.8 KB (23790 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ac249cab7023411f8a5907f3a76e9ea920d08417bb843a490be5713136db3e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af971c76faaef52be66fc01361500e52479d9bd3de8c61e1ef111fba60d5dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f8cd16a2143448bb838f761683fc0d0414b211efd908c29739ea8fd5596ca`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ea935f106a5cac5c3db1cf082812746503193aad9a99f38a4b21f224a57e1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 120.8 KB (120773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63311bdf55b9f3cf77efa26b0da012e373d170b987229f428ce76b886bbce469`  
		Last Modified: Wed, 02 Apr 2025 00:26:44 GMT  
		Size: 2.0 MB (1989465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1d29b03fe2e901538845f42fc32d02e219b7ee32ae4e96d693d524c107f489`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bd8da7aa9a5f757c9aa94050d20b6125e7db478d3d09d066d7bacc647e82cd`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:ad5f230ec532bb07cca752d58c44405687441c7cf07466de1abb8010fe83444b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 KB (117724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e862b1f07efa9790536488995533c7e658e410b55494d4f40578655c76e97e96`

```dockerfile
```

-	Layers:
	-	`sha256:2ae3d7cc25dc211d941164751cecdab1653e411fd74ac6d8792c5b3d72661cc4`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14ce594178b9c4afdf8d733cda3d894e4a9ad61c28d1ac8f7768f95d1c8f3b0b`  
		Last Modified: Wed, 02 Apr 2025 00:26:44 GMT  
		Size: 24.0 KB (23987 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:d4bdd5dcadda94a10fe78fdbf45d948bbfaa8233c6747b530c9e60319c7ba800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3154682685d8fd270595d40c1049cb408aed0282f2c747604db8442fcef5dfe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645c39e6b0ed26b821f36985348fb5422ae3b6196b7cf12ef50dda5a81d2b93`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4567ac7ea6d13e132381838b339c502058075a6fc0b18186ab1799070146919f`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 109.5 KB (109488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b78d96d6f34941f27c987768132a4c5c18ef33bd672132df7d9c5a820399226`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 2.0 MB (1959719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b507bd921881822a186cd02039a745dad142b6e8030ef7de46647172ec3830f`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5982dc98a348c1424c4189f2fc4e046ddfa92211012c880445f8c8f587fcc8`  
		Last Modified: Wed, 02 Apr 2025 00:02:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:a8fcd0e85c073ee5e2cb2181ec295a8a17487566fd2c86ae081021eb5c246d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 KB (117320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b74d45db45f5c8f0ff0f375a08d4173e6d117f52c764d692162cc3c7ce2779`

```dockerfile
```

-	Layers:
	-	`sha256:200655427be8ca8fd2a9527ab234f19e1ae2927df5ae049b42f413365ecc92d9`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9ea6164d6c395a7b52b1395f9884889dd65a2f2aabf838e84561eeb87890b6c`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 23.7 KB (23732 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:846bb02f30ec4006d9b170f8e2fac3617b994e1d5ffbfcbd872c7d916523b4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022d4e1e17a86c0612d17c441ef3227d9042c46d5feecdd9c2a273b8314469e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81a068108debd592bc5100e24523483d0e5439f65b1c2eac8795522da51a6f0`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1b08fecb6beefd2da11b480a18e59255878a54a949bf6bfd470917dcafe91a`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aeecda3ee3acaf18a7673b403236cbe8d93f545f12bc55621b6f37e513900a5`  
		Last Modified: Wed, 02 Apr 2025 00:31:25 GMT  
		Size: 2.1 MB (2091349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b592e99d4871d2d634a039a4d058bed8d83febeccf5444e606b4420f0aa99c6`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c78b4428d40f07afd310ae82ed6fba84a4614528eb42ab1f92520bac7a191e0`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:1656858c9dc9f1197d5b06660d09e4b57f90eed888dacf469ef312f4662e332b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 KB (115604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6a6900dce886d3fa69d25d431a1266fa1944b76e6ba8d139a5d00c0adaed75`

```dockerfile
```

-	Layers:
	-	`sha256:ec185783a159561468b1b9fadb3fd45605c017f8b76fb472b8202218447896c0`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:236149af7dac34fda2172de648c11f6afaa5c6e6566f2a909ad14f671f3c9008`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; riscv64

```console
$ docker pull memcached@sha256:b2d20d9478f0865295f104d69a10a6af47a42a19e0dce14f29edb38774033203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e583bfbee3cc9a94a7b502b1a173f9bf4111fca05ea1278df906891196781025`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf0ec129ec8a2b4d4a1c63ccbf427d2a09e4964506f173b2d50e16da5c5d85d`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87ff2734bb4c56d7bc73ec0ff994ec23d27330caef800d8833aabe135a40c16`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 107.9 KB (107853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efd9838e543fe84c79d3055949dc5f19a024e408550ed536f137c7c1d82dc49`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 1.9 MB (1932539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98def9beaf0eda5e2c72d1bb51c0ba6fd3c4fa353bd2ffaa71c769fc1e24e097`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ed44c8b9815cf9aebd7cb9e2526354718cbcda21e982ef1644179e23f3ed68`  
		Last Modified: Wed, 02 Apr 2025 02:42:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:b79d62e7bee66523ce599bf19665532e58184f1418dcaa75319ae276df7e7102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 KB (115600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc405e5fbc58e4cbffe75922414fde14af323b70005eec6bd80a84057139b80`

```dockerfile
```

-	Layers:
	-	`sha256:f73a53dbdd9178f81244bf32411a1b2748d2a982b43a387ffa12e397da212ac3`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 91.7 KB (91736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41960c07a99d18bed2becce19308f78dbc107450842b1b59bdb2583336c463c8`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:3f70ed54bc6d6486a26fa5d844d30d158f78ee530a9b9ad92d9ee0165bbe3b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5620401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efb254b83b2d2bcf8ea4b50253aca87b5bc46f9f5593b6829b17550790a8f00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e7532ce01b9a31f1f3df73165c991b23b03e88dca43c46f5cc24237fc103d3`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff362c9247c7186b179ab36b3f74241e85aacd9e6bca6d4ef92adad9cfb9e2cd`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 113.5 KB (113461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8290f37bed0ef8feae03102a7631bc1d855099e839e088b703d3abbaf3883921`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 2.0 MB (2038025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b66de72a4b2ca75ad48d4f2e31e85116103f8e920c92abeebfcbe8a523bc048`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f9594fc6f70b3bc4eca62bf52dbc1accfd31976eef6d947935500066ec5a66`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:6000519346e0e698f4e7b53de4fcdb0dc0a7295e922b1ddf5821c39083d85aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 KB (115471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c794c1f5316b791d894d4cb76365cfe77788960fbfb22ec98b8fc72b26bd0e3`

```dockerfile
```

-	Layers:
	-	`sha256:4df28bd3243c0b3247802e9fbda82c25885df47aeb6adc72737fa52615c9d38a`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbf6a1d4a771c26772accd7269d7279e63402148a1eda5a7d29db4ac1101662d`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 23.8 KB (23789 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:0f92cdf1ca059c3b747f95328ed9e8de40866896657cb2b73148be36331efc02
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

### `memcached:1.6-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:15c127398e9bb6bdfdbd6689b817964617401f2d9ca294758323011b3bb09350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33021901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f40f7fb4f0d5e586a146a0a994596292ea1e784ca1657eed1192b2fe17a003c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62639a9e53d980a0e86e3b54ae34e1e913a7f6cebd1bce7741e629047b732896`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5783d9aa8a04d558f9d1d5407d3f6dddb064b0a670738a5cbc480866bbc1a30`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.5 MB (2492219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609bfa774ee059a5d07cc14920af077ac7de9039c567f38164ea31f5eb04d3ba`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.3 MB (2302838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062ee789e2fd31345a9db851ddb0616c67ac7a4ea84e3a0e953af88faa98e3e5`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8416b27aabc571df320856a2ff533825bcbfc2fa602782561ff6b1a0449b821`  
		Last Modified: Wed, 21 May 2025 23:16:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7b5eaaa81772b0dc7377f0c8a8d41bb09c38c1a07292c0e0bef5654ceef3a28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c8287d2eb936f10093c74288a99d09a35c07df6033435ba68847dba2b0fdff`

```dockerfile
```

-	Layers:
	-	`sha256:f5c222a0451ee4a8115a7a9421176131c1481dd511e4ec028e050fdf94e7b741`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.3 MB (2308990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01ac10f70adef13c64045d3be5956b00caafe800e1fab7640f6eaa5f9ea66864`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:9d0d272209b7fd9922e4184de83ab429d527ad56c2f92a6a262cb88cf331551e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30087755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8113ec8739204304b1054312c93717e8c84189d23a003648ffa966d472462cad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01741d1d3bd96678d0f5dccb883892b5af0a3ffb6fe1abaf71cfa8d27579819`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e33674278ab7a59427b75a5c5a4fc74379bdc2cea1105e212becedfd13aadc`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.1 MB (2097064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c00b2be2834a255d33718d0903d2637ed005c981ee3d72a52654f7e0aed5e78`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.2 MB (2232281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148a70549f08f93b07f1c60ad72af807c88405d06687d9fe374648b9a484d40e`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93adc89552cc46d51abc366499a6fac900badfa05b8a0c8c604a7e4ac0cae40`  
		Last Modified: Wed, 21 May 2025 23:46:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7659c54d461b01b9e2062f0a8843b75b7d6a793c3d358a339b78e071770dcbd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2338302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af770cd911aab0856b542fdf7bc835ddf01b1ce26aa176b7b9cacfbc9388fb2d`

```dockerfile
```

-	Layers:
	-	`sha256:6d50a9e0dd879a75ce6c9396bd03c5ecb9beefd32a2d5bd6cf54f36341327685`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.3 MB (2312836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f3107fa09f2c0b66f32bebd5a1bb01208c84b9fa1da768bf5a5dbd20ca500d0`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v7

```console
$ docker pull memcached@sha256:95630a66e2d5c3a453ccc0f22d18ce0a297f1f21536938ff8f1b93c86b9cfbea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28065225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127e001dab188acb98ae7340be866c4c3ae686a9285cf40bd10f9dc702a73ee9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b5a50ba24d961f5862446c5e48fe0c5dbf9acfb0a3718255dd76fab71e84a7`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4adc063a4b96db7c50bcc78cd236a7102a3c31a61fb4216967b2cdcab50c24`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 1.9 MB (1946317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26fc15d35761b3f0c7797ea1ffc39ab51d4227089df7d6b5d2a075730795d20`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 2.2 MB (2184474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64f51527fd9673b0b39f52e4d608185f9461b4282e581e5ef1ce245bdc451e8`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138b4847c3beba31cf3c1807f17ce0b970ec15f04604f92ac076ff994c1a0f68`  
		Last Modified: Wed, 21 May 2025 23:49:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2f6b92592e3f57dbba3221b48b0dce566be344c3e646a89421cfc68ac2827925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857e0ef0a015c3e4c292fe0a24e960bbfba6c8f5844e8022a8d5c11a52d798c8`

```dockerfile
```

-	Layers:
	-	`sha256:7fb0e5e8b1ea53e4ba20b1cee752d37de3b49eaa2c057aea103fb67ad94a2cf5`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 2.3 MB (2311273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:210181bb919654e239b27e79e0a1003bde8ec7d3dd27841dfb0f95d0c62d23d4`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4fc35e2dfad1e5506199e79f54d5400afd22aee2bb1fe0b5e554d051c7c38d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32711358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d9217ce2913b829164781088c527a86fb1d43a48403bfd92c09a9ce7fd4c95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661e0135b0352aad675030e66bdddcf402a36cea02deb2532b0a24d5ba27554`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e7084e0aea669193e1cab086c096bd0764a05f1bf138e1f7c8f0c04eaf3b52`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.4 MB (2355810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259807b0c15878094bf0f3b13afedc0ef32d7eb679af66072ae18096127d72e1`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.3 MB (2288755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacab3ed6c99f53a622eefcda0dee8f57e377bfb97e7f57674e5030b7172988c`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12316079cc5378e29c63fc769e3686207ce41caec7ed76e8e5bb2c3e3b9a4938`  
		Last Modified: Thu, 22 May 2025 00:10:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:ed76bdc15573ee04e086b0a05bfe7056bb260ef0625d8fca2b4c89bd490db508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282362d3d316c5b5bd6b78ff5cfdd9be97d18c3c0018244eeac32f5a123b7d24`

```dockerfile
```

-	Layers:
	-	`sha256:f50a38ae76734a0eff8b24f4e99acd0d1bdb9ab848e04f9ddbcdcf08aadbe908`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.3 MB (2309305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ec44f0bfbd8d8065048e9d7bc8c90c0dcc460586efa613acacb43cb444f3c91`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 25.5 KB (25516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:427a7ad7f639e7cbf4161751cad9450044cbfaf6be8180abc51e01f68cad186c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33962949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a7e05a07d6b637c8752b13cee1ed7a5ebe2a4ef846c0eecaf4b7904d07ff4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d0594fdf9f07f23d90458a489d7972ab011bc5cca342af82850c3e9c024e3e`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4797e4e934c0c059a34c8b9d6c2adc40dece3f2ba61185edfa1c36591ef3549f`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.5 MB (2502658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7cc241a1440cfefd9f5b88cb6233b9ee820398da0c74155859c3114dd0646c`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.3 MB (2251292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cacd3ce01b0221992568e7179a1408774519b7dfbfc1daf37095764ae9bf16`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4abb18b4fabd731df2a3dbba62cd3f6de6cc4a6ab8419827bcbeb87641c4ad7`  
		Last Modified: Wed, 21 May 2025 23:16:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3c7de609f262a2ab1ddafedf272ac08f1eded0a2b08450f76dbd927b4b746f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfd69fc1ff5ceb8e449d8374c86427aafe41200a46c937aee60fce7a21ebf13`

```dockerfile
```

-	Layers:
	-	`sha256:87803ae24543fc1d1ecf0d1af68207e9714fd56829bab2354f9dd3940e3cf240`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.3 MB (2306133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b6feaf94b04b7737bdbf12b7c3f15ea0f7c46ead6614b9a46a82b87b5e5c75`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:55e7557e19928aa1991fbb59dcb75ea75b5b87115b772f36fd7302618c031468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32774540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1d55a83743e8701a5f0aacd60bd4260744537318e9335e6f681f765a2f536e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Wed, 21 May 2025 22:28:22 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00be87e076613598c61cb34d1eab1a04e74cb16c312c6b2737aaa5b2f54f0cad`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4fdba1c45e7b51399330c05d6b7e619f96cc0ed80cfd6bc75722cf5c982105`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 1.9 MB (1944079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d0d8b3f93dba36eb05fef21a3cda9faaf4e064e161fb87965839f9da4a2a20`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 2.3 MB (2317092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d4a6285da352b0857160c9194204e6801269736b4b18ca39bead26e9be8345`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d044aab1c575f4ebf7752dd0c9d988fc02e7b6f86316622b1678cea3cb9ca44`  
		Last Modified: Thu, 22 May 2025 00:11:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:048fdf15ee7c39e63ec03618e8587191e3915649f1b0076574f19773f9ccf067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c546fba658eb64c00d4036d1ac6c25e4a6f0b1681950c03a94ffc3954fb0d5c9`

```dockerfile
```

-	Layers:
	-	`sha256:2d39a6be744c7e579e7d4147fdc82a19956c6223fcb98601955e9a0a5d1e9e2e`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 25.2 KB (25216 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:3e871b866378795839b5bac555437a97646aa6f1c2abccdd182fe6b8ea84c983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37197690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9129b120bccf4a13f93ae0e47a4046e9ab94b4ff2d8de473eb248683b2802a6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Wed, 21 May 2025 22:28:16 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50fa062d3f9b2ead925a10e36e54327c0aae0c280d34e1075bcf82708310f13`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c345e70ea367cfeb023138dcae0d694e941f247957111430bd191f08181ef2b`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.7 MB (2710200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bd27f00915f27350ad09f9ca295e22cc787fe09c28db9040ad1bfcbfb1508d`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.4 MB (2419066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eee08866234c70e5aa7c719d396e45b9f8955b9a790d0654fd365d3c76c73d5`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0641a69e7e1f05a1544285cb3b709a8b9228ca6d1e6d96c66a0ae3f60cbc246f`  
		Last Modified: Wed, 21 May 2025 23:38:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:284c98dff5f2a0ad150bd4211a1db129fd87428ca2dde05427a3d4470d23d784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2338855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a8b8e6552c03d26ecc498bc8ff9ea559e55ea267d60e50335e46a93423df9`

```dockerfile
```

-	Layers:
	-	`sha256:529db81d9e88463a9e87c4177e55e182fb444bfc991ca4c30bab1e9cb81936e2`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.3 MB (2313462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b94ad3350b6fceb471a3b45c6d44ab4dfbfcbe1d28aeff91254919fe0cfdc04`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 25.4 KB (25393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:949a4a30fca21f6a731aafd862d71f8b49ba9a8499f7d5fee52e7dd0cc5481c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31304875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae677ba0b021f969e80917c5866c4ad53dc0c6406cf6c32e1453b0bab9152d77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2f122115cc85d695acc4bd6bce955e259f1bbad28dc671e212eaf4793195e7`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c30cebca59bfd8fbcc77d6107f2e1f0ee44ec402a34a0a31604aa524a390a1`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.2 MB (2156961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c2d1ec6d6a0ae48f133bf8b323c42f088f609830eba9aba813c3f613ce67e5`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.3 MB (2263596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085b757a938317b0432d2c6e577bb26b74869f14bdb090efd1e3108581b8acac`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f05beedc084a77558e99193cabc217fa002c1042529df98c5208f1d819d325`  
		Last Modified: Wed, 21 May 2025 23:28:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:25e3d5e4f2c4ca9668835e3673d0f663e4034016efbd9381b33ae2b961dd7d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e5415c88643fa263a323da5616aca4b27b38aab4197943da866f83fae75f84`

```dockerfile
```

-	Layers:
	-	`sha256:acc18fbdd9cb8d010d8ea1d191203d0c8e33ba9dce4fe255c1f8419cb63173e7`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.3 MB (2308704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa9690c26e582bfe6c776880fd91701c7a69b74e44fa78dd536af4fc3e871259`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.38`

```console
$ docker pull memcached@sha256:0f92cdf1ca059c3b747f95328ed9e8de40866896657cb2b73148be36331efc02
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

### `memcached:1.6.38` - linux; amd64

```console
$ docker pull memcached@sha256:15c127398e9bb6bdfdbd6689b817964617401f2d9ca294758323011b3bb09350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33021901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f40f7fb4f0d5e586a146a0a994596292ea1e784ca1657eed1192b2fe17a003c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62639a9e53d980a0e86e3b54ae34e1e913a7f6cebd1bce7741e629047b732896`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5783d9aa8a04d558f9d1d5407d3f6dddb064b0a670738a5cbc480866bbc1a30`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.5 MB (2492219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609bfa774ee059a5d07cc14920af077ac7de9039c567f38164ea31f5eb04d3ba`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.3 MB (2302838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062ee789e2fd31345a9db851ddb0616c67ac7a4ea84e3a0e953af88faa98e3e5`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8416b27aabc571df320856a2ff533825bcbfc2fa602782561ff6b1a0449b821`  
		Last Modified: Wed, 21 May 2025 23:16:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:7b5eaaa81772b0dc7377f0c8a8d41bb09c38c1a07292c0e0bef5654ceef3a28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c8287d2eb936f10093c74288a99d09a35c07df6033435ba68847dba2b0fdff`

```dockerfile
```

-	Layers:
	-	`sha256:f5c222a0451ee4a8115a7a9421176131c1481dd511e4ec028e050fdf94e7b741`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.3 MB (2308990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01ac10f70adef13c64045d3be5956b00caafe800e1fab7640f6eaa5f9ea66864`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; arm variant v5

```console
$ docker pull memcached@sha256:9d0d272209b7fd9922e4184de83ab429d527ad56c2f92a6a262cb88cf331551e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30087755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8113ec8739204304b1054312c93717e8c84189d23a003648ffa966d472462cad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01741d1d3bd96678d0f5dccb883892b5af0a3ffb6fe1abaf71cfa8d27579819`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e33674278ab7a59427b75a5c5a4fc74379bdc2cea1105e212becedfd13aadc`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.1 MB (2097064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c00b2be2834a255d33718d0903d2637ed005c981ee3d72a52654f7e0aed5e78`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.2 MB (2232281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148a70549f08f93b07f1c60ad72af807c88405d06687d9fe374648b9a484d40e`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93adc89552cc46d51abc366499a6fac900badfa05b8a0c8c604a7e4ac0cae40`  
		Last Modified: Wed, 21 May 2025 23:46:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:7659c54d461b01b9e2062f0a8843b75b7d6a793c3d358a339b78e071770dcbd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2338302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af770cd911aab0856b542fdf7bc835ddf01b1ce26aa176b7b9cacfbc9388fb2d`

```dockerfile
```

-	Layers:
	-	`sha256:6d50a9e0dd879a75ce6c9396bd03c5ecb9beefd32a2d5bd6cf54f36341327685`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.3 MB (2312836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f3107fa09f2c0b66f32bebd5a1bb01208c84b9fa1da768bf5a5dbd20ca500d0`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; arm variant v7

```console
$ docker pull memcached@sha256:95630a66e2d5c3a453ccc0f22d18ce0a297f1f21536938ff8f1b93c86b9cfbea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28065225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127e001dab188acb98ae7340be866c4c3ae686a9285cf40bd10f9dc702a73ee9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b5a50ba24d961f5862446c5e48fe0c5dbf9acfb0a3718255dd76fab71e84a7`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4adc063a4b96db7c50bcc78cd236a7102a3c31a61fb4216967b2cdcab50c24`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 1.9 MB (1946317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26fc15d35761b3f0c7797ea1ffc39ab51d4227089df7d6b5d2a075730795d20`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 2.2 MB (2184474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64f51527fd9673b0b39f52e4d608185f9461b4282e581e5ef1ce245bdc451e8`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138b4847c3beba31cf3c1807f17ce0b970ec15f04604f92ac076ff994c1a0f68`  
		Last Modified: Wed, 21 May 2025 23:49:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:2f6b92592e3f57dbba3221b48b0dce566be344c3e646a89421cfc68ac2827925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857e0ef0a015c3e4c292fe0a24e960bbfba6c8f5844e8022a8d5c11a52d798c8`

```dockerfile
```

-	Layers:
	-	`sha256:7fb0e5e8b1ea53e4ba20b1cee752d37de3b49eaa2c057aea103fb67ad94a2cf5`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 2.3 MB (2311273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:210181bb919654e239b27e79e0a1003bde8ec7d3dd27841dfb0f95d0c62d23d4`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4fc35e2dfad1e5506199e79f54d5400afd22aee2bb1fe0b5e554d051c7c38d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32711358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d9217ce2913b829164781088c527a86fb1d43a48403bfd92c09a9ce7fd4c95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661e0135b0352aad675030e66bdddcf402a36cea02deb2532b0a24d5ba27554`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e7084e0aea669193e1cab086c096bd0764a05f1bf138e1f7c8f0c04eaf3b52`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.4 MB (2355810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259807b0c15878094bf0f3b13afedc0ef32d7eb679af66072ae18096127d72e1`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.3 MB (2288755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacab3ed6c99f53a622eefcda0dee8f57e377bfb97e7f57674e5030b7172988c`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12316079cc5378e29c63fc769e3686207ce41caec7ed76e8e5bb2c3e3b9a4938`  
		Last Modified: Thu, 22 May 2025 00:10:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:ed76bdc15573ee04e086b0a05bfe7056bb260ef0625d8fca2b4c89bd490db508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282362d3d316c5b5bd6b78ff5cfdd9be97d18c3c0018244eeac32f5a123b7d24`

```dockerfile
```

-	Layers:
	-	`sha256:f50a38ae76734a0eff8b24f4e99acd0d1bdb9ab848e04f9ddbcdcf08aadbe908`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.3 MB (2309305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ec44f0bfbd8d8065048e9d7bc8c90c0dcc460586efa613acacb43cb444f3c91`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 25.5 KB (25516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; 386

```console
$ docker pull memcached@sha256:427a7ad7f639e7cbf4161751cad9450044cbfaf6be8180abc51e01f68cad186c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33962949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a7e05a07d6b637c8752b13cee1ed7a5ebe2a4ef846c0eecaf4b7904d07ff4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d0594fdf9f07f23d90458a489d7972ab011bc5cca342af82850c3e9c024e3e`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4797e4e934c0c059a34c8b9d6c2adc40dece3f2ba61185edfa1c36591ef3549f`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.5 MB (2502658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7cc241a1440cfefd9f5b88cb6233b9ee820398da0c74155859c3114dd0646c`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.3 MB (2251292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cacd3ce01b0221992568e7179a1408774519b7dfbfc1daf37095764ae9bf16`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4abb18b4fabd731df2a3dbba62cd3f6de6cc4a6ab8419827bcbeb87641c4ad7`  
		Last Modified: Wed, 21 May 2025 23:16:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:3c7de609f262a2ab1ddafedf272ac08f1eded0a2b08450f76dbd927b4b746f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfd69fc1ff5ceb8e449d8374c86427aafe41200a46c937aee60fce7a21ebf13`

```dockerfile
```

-	Layers:
	-	`sha256:87803ae24543fc1d1ecf0d1af68207e9714fd56829bab2354f9dd3940e3cf240`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.3 MB (2306133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b6feaf94b04b7737bdbf12b7c3f15ea0f7c46ead6614b9a46a82b87b5e5c75`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; mips64le

```console
$ docker pull memcached@sha256:55e7557e19928aa1991fbb59dcb75ea75b5b87115b772f36fd7302618c031468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32774540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1d55a83743e8701a5f0aacd60bd4260744537318e9335e6f681f765a2f536e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Wed, 21 May 2025 22:28:22 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00be87e076613598c61cb34d1eab1a04e74cb16c312c6b2737aaa5b2f54f0cad`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4fdba1c45e7b51399330c05d6b7e619f96cc0ed80cfd6bc75722cf5c982105`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 1.9 MB (1944079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d0d8b3f93dba36eb05fef21a3cda9faaf4e064e161fb87965839f9da4a2a20`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 2.3 MB (2317092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d4a6285da352b0857160c9194204e6801269736b4b18ca39bead26e9be8345`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d044aab1c575f4ebf7752dd0c9d988fc02e7b6f86316622b1678cea3cb9ca44`  
		Last Modified: Thu, 22 May 2025 00:11:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:048fdf15ee7c39e63ec03618e8587191e3915649f1b0076574f19773f9ccf067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c546fba658eb64c00d4036d1ac6c25e4a6f0b1681950c03a94ffc3954fb0d5c9`

```dockerfile
```

-	Layers:
	-	`sha256:2d39a6be744c7e579e7d4147fdc82a19956c6223fcb98601955e9a0a5d1e9e2e`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 25.2 KB (25216 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; ppc64le

```console
$ docker pull memcached@sha256:3e871b866378795839b5bac555437a97646aa6f1c2abccdd182fe6b8ea84c983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37197690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9129b120bccf4a13f93ae0e47a4046e9ab94b4ff2d8de473eb248683b2802a6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Wed, 21 May 2025 22:28:16 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50fa062d3f9b2ead925a10e36e54327c0aae0c280d34e1075bcf82708310f13`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c345e70ea367cfeb023138dcae0d694e941f247957111430bd191f08181ef2b`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.7 MB (2710200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bd27f00915f27350ad09f9ca295e22cc787fe09c28db9040ad1bfcbfb1508d`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.4 MB (2419066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eee08866234c70e5aa7c719d396e45b9f8955b9a790d0654fd365d3c76c73d5`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0641a69e7e1f05a1544285cb3b709a8b9228ca6d1e6d96c66a0ae3f60cbc246f`  
		Last Modified: Wed, 21 May 2025 23:38:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:284c98dff5f2a0ad150bd4211a1db129fd87428ca2dde05427a3d4470d23d784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2338855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a8b8e6552c03d26ecc498bc8ff9ea559e55ea267d60e50335e46a93423df9`

```dockerfile
```

-	Layers:
	-	`sha256:529db81d9e88463a9e87c4177e55e182fb444bfc991ca4c30bab1e9cb81936e2`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.3 MB (2313462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b94ad3350b6fceb471a3b45c6d44ab4dfbfcbe1d28aeff91254919fe0cfdc04`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 25.4 KB (25393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38` - linux; s390x

```console
$ docker pull memcached@sha256:949a4a30fca21f6a731aafd862d71f8b49ba9a8499f7d5fee52e7dd0cc5481c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31304875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae677ba0b021f969e80917c5866c4ad53dc0c6406cf6c32e1453b0bab9152d77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2f122115cc85d695acc4bd6bce955e259f1bbad28dc671e212eaf4793195e7`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c30cebca59bfd8fbcc77d6107f2e1f0ee44ec402a34a0a31604aa524a390a1`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.2 MB (2156961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c2d1ec6d6a0ae48f133bf8b323c42f088f609830eba9aba813c3f613ce67e5`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.3 MB (2263596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085b757a938317b0432d2c6e577bb26b74869f14bdb090efd1e3108581b8acac`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f05beedc084a77558e99193cabc217fa002c1042529df98c5208f1d819d325`  
		Last Modified: Wed, 21 May 2025 23:28:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38` - unknown; unknown

```console
$ docker pull memcached@sha256:25e3d5e4f2c4ca9668835e3673d0f663e4034016efbd9381b33ae2b961dd7d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e5415c88643fa263a323da5616aca4b27b38aab4197943da866f83fae75f84`

```dockerfile
```

-	Layers:
	-	`sha256:acc18fbdd9cb8d010d8ea1d191203d0c8e33ba9dce4fe255c1f8419cb63173e7`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.3 MB (2308704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa9690c26e582bfe6c776880fd91701c7a69b74e44fa78dd536af4fc3e871259`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.38-alpine`

```console
$ docker pull memcached@sha256:5ac71d3889701bd0750d35b06762ab7efc873ef29d7a43848ef5b0dc30a0dad4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
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

### `memcached:1.6.38-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:90ff65aa470196afc5361ee16ebb344c3fb42f6317c16e4babaec1c79ad476ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5746542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c733c89a0ba90440ee956db059a3616a71a5e394c8dc9c9f6c1a9214b745d771`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3211cc8fb7612d73a250fd41e8ce1b264d4bafde9010ea586db45a946cb9dd79`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2692de63622aa06cd0ab32cbab5ebaac7c5c72f7f69c9c81711ec7196affb045`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 104.7 KB (104697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3694ff7984b804f1b2422eccdace864bc5b29564ff174a1e81f6b15ad9ad64e5`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 2.0 MB (1998247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a875c9e38db3d48eaf047d806f55e1ad705d891e17b24e691c6ae06b04416de`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d8aff7b7f4a9a5b7acb0870b99bc082dab792802823f42cb3df6bac425a03a`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:815522b8bf7a5c758712c55e2dfd2ba153f6d5def56049ebca9689c40b47036e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 KB (117423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e7d1adeedbeaad748f0fb03984aebb1f7b8d7a578733dfed68ae55a4d8aca5`

```dockerfile
```

-	Layers:
	-	`sha256:16f52c61ed51ca807453bbac564f16e1bc7438d019b75b43b432beee3917cf9e`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a618a61037789490baaad3bd81b36e771be572bc09db7bb521a4ea03c2c7199`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 23.8 KB (23790 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ac249cab7023411f8a5907f3a76e9ea920d08417bb843a490be5713136db3e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af971c76faaef52be66fc01361500e52479d9bd3de8c61e1ef111fba60d5dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f8cd16a2143448bb838f761683fc0d0414b211efd908c29739ea8fd5596ca`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ea935f106a5cac5c3db1cf082812746503193aad9a99f38a4b21f224a57e1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 120.8 KB (120773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63311bdf55b9f3cf77efa26b0da012e373d170b987229f428ce76b886bbce469`  
		Last Modified: Wed, 02 Apr 2025 00:26:44 GMT  
		Size: 2.0 MB (1989465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1d29b03fe2e901538845f42fc32d02e219b7ee32ae4e96d693d524c107f489`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bd8da7aa9a5f757c9aa94050d20b6125e7db478d3d09d066d7bacc647e82cd`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ad5f230ec532bb07cca752d58c44405687441c7cf07466de1abb8010fe83444b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 KB (117724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e862b1f07efa9790536488995533c7e658e410b55494d4f40578655c76e97e96`

```dockerfile
```

-	Layers:
	-	`sha256:2ae3d7cc25dc211d941164751cecdab1653e411fd74ac6d8792c5b3d72661cc4`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14ce594178b9c4afdf8d733cda3d894e4a9ad61c28d1ac8f7768f95d1c8f3b0b`  
		Last Modified: Wed, 02 Apr 2025 00:26:44 GMT  
		Size: 24.0 KB (23987 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine` - linux; 386

```console
$ docker pull memcached@sha256:d4bdd5dcadda94a10fe78fdbf45d948bbfaa8233c6747b530c9e60319c7ba800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3154682685d8fd270595d40c1049cb408aed0282f2c747604db8442fcef5dfe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645c39e6b0ed26b821f36985348fb5422ae3b6196b7cf12ef50dda5a81d2b93`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4567ac7ea6d13e132381838b339c502058075a6fc0b18186ab1799070146919f`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 109.5 KB (109488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b78d96d6f34941f27c987768132a4c5c18ef33bd672132df7d9c5a820399226`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 2.0 MB (1959719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b507bd921881822a186cd02039a745dad142b6e8030ef7de46647172ec3830f`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5982dc98a348c1424c4189f2fc4e046ddfa92211012c880445f8c8f587fcc8`  
		Last Modified: Wed, 02 Apr 2025 00:02:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a8fcd0e85c073ee5e2cb2181ec295a8a17487566fd2c86ae081021eb5c246d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 KB (117320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b74d45db45f5c8f0ff0f375a08d4173e6d117f52c764d692162cc3c7ce2779`

```dockerfile
```

-	Layers:
	-	`sha256:200655427be8ca8fd2a9527ab234f19e1ae2927df5ae049b42f413365ecc92d9`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9ea6164d6c395a7b52b1395f9884889dd65a2f2aabf838e84561eeb87890b6c`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 23.7 KB (23732 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:846bb02f30ec4006d9b170f8e2fac3617b994e1d5ffbfcbd872c7d916523b4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022d4e1e17a86c0612d17c441ef3227d9042c46d5feecdd9c2a273b8314469e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81a068108debd592bc5100e24523483d0e5439f65b1c2eac8795522da51a6f0`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1b08fecb6beefd2da11b480a18e59255878a54a949bf6bfd470917dcafe91a`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aeecda3ee3acaf18a7673b403236cbe8d93f545f12bc55621b6f37e513900a5`  
		Last Modified: Wed, 02 Apr 2025 00:31:25 GMT  
		Size: 2.1 MB (2091349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b592e99d4871d2d634a039a4d058bed8d83febeccf5444e606b4420f0aa99c6`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c78b4428d40f07afd310ae82ed6fba84a4614528eb42ab1f92520bac7a191e0`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1656858c9dc9f1197d5b06660d09e4b57f90eed888dacf469ef312f4662e332b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 KB (115604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6a6900dce886d3fa69d25d431a1266fa1944b76e6ba8d139a5d00c0adaed75`

```dockerfile
```

-	Layers:
	-	`sha256:ec185783a159561468b1b9fadb3fd45605c017f8b76fb472b8202218447896c0`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:236149af7dac34fda2172de648c11f6afaa5c6e6566f2a909ad14f671f3c9008`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:b2d20d9478f0865295f104d69a10a6af47a42a19e0dce14f29edb38774033203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e583bfbee3cc9a94a7b502b1a173f9bf4111fca05ea1278df906891196781025`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf0ec129ec8a2b4d4a1c63ccbf427d2a09e4964506f173b2d50e16da5c5d85d`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87ff2734bb4c56d7bc73ec0ff994ec23d27330caef800d8833aabe135a40c16`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 107.9 KB (107853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efd9838e543fe84c79d3055949dc5f19a024e408550ed536f137c7c1d82dc49`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 1.9 MB (1932539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98def9beaf0eda5e2c72d1bb51c0ba6fd3c4fa353bd2ffaa71c769fc1e24e097`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ed44c8b9815cf9aebd7cb9e2526354718cbcda21e982ef1644179e23f3ed68`  
		Last Modified: Wed, 02 Apr 2025 02:42:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b79d62e7bee66523ce599bf19665532e58184f1418dcaa75319ae276df7e7102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 KB (115600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc405e5fbc58e4cbffe75922414fde14af323b70005eec6bd80a84057139b80`

```dockerfile
```

-	Layers:
	-	`sha256:f73a53dbdd9178f81244bf32411a1b2748d2a982b43a387ffa12e397da212ac3`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 91.7 KB (91736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41960c07a99d18bed2becce19308f78dbc107450842b1b59bdb2583336c463c8`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:3f70ed54bc6d6486a26fa5d844d30d158f78ee530a9b9ad92d9ee0165bbe3b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5620401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efb254b83b2d2bcf8ea4b50253aca87b5bc46f9f5593b6829b17550790a8f00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e7532ce01b9a31f1f3df73165c991b23b03e88dca43c46f5cc24237fc103d3`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff362c9247c7186b179ab36b3f74241e85aacd9e6bca6d4ef92adad9cfb9e2cd`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 113.5 KB (113461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8290f37bed0ef8feae03102a7631bc1d855099e839e088b703d3abbaf3883921`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 2.0 MB (2038025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b66de72a4b2ca75ad48d4f2e31e85116103f8e920c92abeebfcbe8a523bc048`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f9594fc6f70b3bc4eca62bf52dbc1accfd31976eef6d947935500066ec5a66`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6000519346e0e698f4e7b53de4fcdb0dc0a7295e922b1ddf5821c39083d85aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 KB (115471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c794c1f5316b791d894d4cb76365cfe77788960fbfb22ec98b8fc72b26bd0e3`

```dockerfile
```

-	Layers:
	-	`sha256:4df28bd3243c0b3247802e9fbda82c25885df47aeb6adc72737fa52615c9d38a`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbf6a1d4a771c26772accd7269d7279e63402148a1eda5a7d29db4ac1101662d`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 23.8 KB (23789 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.38-alpine3.21`

```console
$ docker pull memcached@sha256:5ac71d3889701bd0750d35b06762ab7efc873ef29d7a43848ef5b0dc30a0dad4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
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

### `memcached:1.6.38-alpine3.21` - linux; amd64

```console
$ docker pull memcached@sha256:90ff65aa470196afc5361ee16ebb344c3fb42f6317c16e4babaec1c79ad476ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5746542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c733c89a0ba90440ee956db059a3616a71a5e394c8dc9c9f6c1a9214b745d771`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3211cc8fb7612d73a250fd41e8ce1b264d4bafde9010ea586db45a946cb9dd79`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2692de63622aa06cd0ab32cbab5ebaac7c5c72f7f69c9c81711ec7196affb045`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 104.7 KB (104697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3694ff7984b804f1b2422eccdace864bc5b29564ff174a1e81f6b15ad9ad64e5`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 2.0 MB (1998247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a875c9e38db3d48eaf047d806f55e1ad705d891e17b24e691c6ae06b04416de`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d8aff7b7f4a9a5b7acb0870b99bc082dab792802823f42cb3df6bac425a03a`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:815522b8bf7a5c758712c55e2dfd2ba153f6d5def56049ebca9689c40b47036e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 KB (117423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e7d1adeedbeaad748f0fb03984aebb1f7b8d7a578733dfed68ae55a4d8aca5`

```dockerfile
```

-	Layers:
	-	`sha256:16f52c61ed51ca807453bbac564f16e1bc7438d019b75b43b432beee3917cf9e`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a618a61037789490baaad3bd81b36e771be572bc09db7bb521a4ea03c2c7199`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 23.8 KB (23790 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ac249cab7023411f8a5907f3a76e9ea920d08417bb843a490be5713136db3e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af971c76faaef52be66fc01361500e52479d9bd3de8c61e1ef111fba60d5dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f8cd16a2143448bb838f761683fc0d0414b211efd908c29739ea8fd5596ca`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ea935f106a5cac5c3db1cf082812746503193aad9a99f38a4b21f224a57e1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 120.8 KB (120773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63311bdf55b9f3cf77efa26b0da012e373d170b987229f428ce76b886bbce469`  
		Last Modified: Wed, 02 Apr 2025 00:26:44 GMT  
		Size: 2.0 MB (1989465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1d29b03fe2e901538845f42fc32d02e219b7ee32ae4e96d693d524c107f489`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bd8da7aa9a5f757c9aa94050d20b6125e7db478d3d09d066d7bacc647e82cd`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:ad5f230ec532bb07cca752d58c44405687441c7cf07466de1abb8010fe83444b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 KB (117724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e862b1f07efa9790536488995533c7e658e410b55494d4f40578655c76e97e96`

```dockerfile
```

-	Layers:
	-	`sha256:2ae3d7cc25dc211d941164751cecdab1653e411fd74ac6d8792c5b3d72661cc4`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14ce594178b9c4afdf8d733cda3d894e4a9ad61c28d1ac8f7768f95d1c8f3b0b`  
		Last Modified: Wed, 02 Apr 2025 00:26:44 GMT  
		Size: 24.0 KB (23987 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:d4bdd5dcadda94a10fe78fdbf45d948bbfaa8233c6747b530c9e60319c7ba800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3154682685d8fd270595d40c1049cb408aed0282f2c747604db8442fcef5dfe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645c39e6b0ed26b821f36985348fb5422ae3b6196b7cf12ef50dda5a81d2b93`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4567ac7ea6d13e132381838b339c502058075a6fc0b18186ab1799070146919f`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 109.5 KB (109488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b78d96d6f34941f27c987768132a4c5c18ef33bd672132df7d9c5a820399226`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 2.0 MB (1959719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b507bd921881822a186cd02039a745dad142b6e8030ef7de46647172ec3830f`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5982dc98a348c1424c4189f2fc4e046ddfa92211012c880445f8c8f587fcc8`  
		Last Modified: Wed, 02 Apr 2025 00:02:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:a8fcd0e85c073ee5e2cb2181ec295a8a17487566fd2c86ae081021eb5c246d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 KB (117320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b74d45db45f5c8f0ff0f375a08d4173e6d117f52c764d692162cc3c7ce2779`

```dockerfile
```

-	Layers:
	-	`sha256:200655427be8ca8fd2a9527ab234f19e1ae2927df5ae049b42f413365ecc92d9`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9ea6164d6c395a7b52b1395f9884889dd65a2f2aabf838e84561eeb87890b6c`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 23.7 KB (23732 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:846bb02f30ec4006d9b170f8e2fac3617b994e1d5ffbfcbd872c7d916523b4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022d4e1e17a86c0612d17c441ef3227d9042c46d5feecdd9c2a273b8314469e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81a068108debd592bc5100e24523483d0e5439f65b1c2eac8795522da51a6f0`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1b08fecb6beefd2da11b480a18e59255878a54a949bf6bfd470917dcafe91a`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aeecda3ee3acaf18a7673b403236cbe8d93f545f12bc55621b6f37e513900a5`  
		Last Modified: Wed, 02 Apr 2025 00:31:25 GMT  
		Size: 2.1 MB (2091349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b592e99d4871d2d634a039a4d058bed8d83febeccf5444e606b4420f0aa99c6`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c78b4428d40f07afd310ae82ed6fba84a4614528eb42ab1f92520bac7a191e0`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:1656858c9dc9f1197d5b06660d09e4b57f90eed888dacf469ef312f4662e332b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 KB (115604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6a6900dce886d3fa69d25d431a1266fa1944b76e6ba8d139a5d00c0adaed75`

```dockerfile
```

-	Layers:
	-	`sha256:ec185783a159561468b1b9fadb3fd45605c017f8b76fb472b8202218447896c0`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:236149af7dac34fda2172de648c11f6afaa5c6e6566f2a909ad14f671f3c9008`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine3.21` - linux; riscv64

```console
$ docker pull memcached@sha256:b2d20d9478f0865295f104d69a10a6af47a42a19e0dce14f29edb38774033203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e583bfbee3cc9a94a7b502b1a173f9bf4111fca05ea1278df906891196781025`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf0ec129ec8a2b4d4a1c63ccbf427d2a09e4964506f173b2d50e16da5c5d85d`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87ff2734bb4c56d7bc73ec0ff994ec23d27330caef800d8833aabe135a40c16`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 107.9 KB (107853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efd9838e543fe84c79d3055949dc5f19a024e408550ed536f137c7c1d82dc49`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 1.9 MB (1932539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98def9beaf0eda5e2c72d1bb51c0ba6fd3c4fa353bd2ffaa71c769fc1e24e097`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ed44c8b9815cf9aebd7cb9e2526354718cbcda21e982ef1644179e23f3ed68`  
		Last Modified: Wed, 02 Apr 2025 02:42:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:b79d62e7bee66523ce599bf19665532e58184f1418dcaa75319ae276df7e7102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 KB (115600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc405e5fbc58e4cbffe75922414fde14af323b70005eec6bd80a84057139b80`

```dockerfile
```

-	Layers:
	-	`sha256:f73a53dbdd9178f81244bf32411a1b2748d2a982b43a387ffa12e397da212ac3`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 91.7 KB (91736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41960c07a99d18bed2becce19308f78dbc107450842b1b59bdb2583336c463c8`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:3f70ed54bc6d6486a26fa5d844d30d158f78ee530a9b9ad92d9ee0165bbe3b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5620401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efb254b83b2d2bcf8ea4b50253aca87b5bc46f9f5593b6829b17550790a8f00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e7532ce01b9a31f1f3df73165c991b23b03e88dca43c46f5cc24237fc103d3`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff362c9247c7186b179ab36b3f74241e85aacd9e6bca6d4ef92adad9cfb9e2cd`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 113.5 KB (113461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8290f37bed0ef8feae03102a7631bc1d855099e839e088b703d3abbaf3883921`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 2.0 MB (2038025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b66de72a4b2ca75ad48d4f2e31e85116103f8e920c92abeebfcbe8a523bc048`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f9594fc6f70b3bc4eca62bf52dbc1accfd31976eef6d947935500066ec5a66`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:6000519346e0e698f4e7b53de4fcdb0dc0a7295e922b1ddf5821c39083d85aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 KB (115471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c794c1f5316b791d894d4cb76365cfe77788960fbfb22ec98b8fc72b26bd0e3`

```dockerfile
```

-	Layers:
	-	`sha256:4df28bd3243c0b3247802e9fbda82c25885df47aeb6adc72737fa52615c9d38a`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbf6a1d4a771c26772accd7269d7279e63402148a1eda5a7d29db4ac1101662d`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 23.8 KB (23789 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.38-bookworm`

```console
$ docker pull memcached@sha256:0f92cdf1ca059c3b747f95328ed9e8de40866896657cb2b73148be36331efc02
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

### `memcached:1.6.38-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:15c127398e9bb6bdfdbd6689b817964617401f2d9ca294758323011b3bb09350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33021901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f40f7fb4f0d5e586a146a0a994596292ea1e784ca1657eed1192b2fe17a003c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62639a9e53d980a0e86e3b54ae34e1e913a7f6cebd1bce7741e629047b732896`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5783d9aa8a04d558f9d1d5407d3f6dddb064b0a670738a5cbc480866bbc1a30`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.5 MB (2492219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609bfa774ee059a5d07cc14920af077ac7de9039c567f38164ea31f5eb04d3ba`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.3 MB (2302838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062ee789e2fd31345a9db851ddb0616c67ac7a4ea84e3a0e953af88faa98e3e5`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8416b27aabc571df320856a2ff533825bcbfc2fa602782561ff6b1a0449b821`  
		Last Modified: Wed, 21 May 2025 23:16:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7b5eaaa81772b0dc7377f0c8a8d41bb09c38c1a07292c0e0bef5654ceef3a28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c8287d2eb936f10093c74288a99d09a35c07df6033435ba68847dba2b0fdff`

```dockerfile
```

-	Layers:
	-	`sha256:f5c222a0451ee4a8115a7a9421176131c1481dd511e4ec028e050fdf94e7b741`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.3 MB (2308990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01ac10f70adef13c64045d3be5956b00caafe800e1fab7640f6eaa5f9ea66864`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:9d0d272209b7fd9922e4184de83ab429d527ad56c2f92a6a262cb88cf331551e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30087755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8113ec8739204304b1054312c93717e8c84189d23a003648ffa966d472462cad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01741d1d3bd96678d0f5dccb883892b5af0a3ffb6fe1abaf71cfa8d27579819`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e33674278ab7a59427b75a5c5a4fc74379bdc2cea1105e212becedfd13aadc`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.1 MB (2097064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c00b2be2834a255d33718d0903d2637ed005c981ee3d72a52654f7e0aed5e78`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.2 MB (2232281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148a70549f08f93b07f1c60ad72af807c88405d06687d9fe374648b9a484d40e`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93adc89552cc46d51abc366499a6fac900badfa05b8a0c8c604a7e4ac0cae40`  
		Last Modified: Wed, 21 May 2025 23:46:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7659c54d461b01b9e2062f0a8843b75b7d6a793c3d358a339b78e071770dcbd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2338302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af770cd911aab0856b542fdf7bc835ddf01b1ce26aa176b7b9cacfbc9388fb2d`

```dockerfile
```

-	Layers:
	-	`sha256:6d50a9e0dd879a75ce6c9396bd03c5ecb9beefd32a2d5bd6cf54f36341327685`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.3 MB (2312836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f3107fa09f2c0b66f32bebd5a1bb01208c84b9fa1da768bf5a5dbd20ca500d0`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; arm variant v7

```console
$ docker pull memcached@sha256:95630a66e2d5c3a453ccc0f22d18ce0a297f1f21536938ff8f1b93c86b9cfbea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28065225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127e001dab188acb98ae7340be866c4c3ae686a9285cf40bd10f9dc702a73ee9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b5a50ba24d961f5862446c5e48fe0c5dbf9acfb0a3718255dd76fab71e84a7`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4adc063a4b96db7c50bcc78cd236a7102a3c31a61fb4216967b2cdcab50c24`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 1.9 MB (1946317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26fc15d35761b3f0c7797ea1ffc39ab51d4227089df7d6b5d2a075730795d20`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 2.2 MB (2184474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64f51527fd9673b0b39f52e4d608185f9461b4282e581e5ef1ce245bdc451e8`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138b4847c3beba31cf3c1807f17ce0b970ec15f04604f92ac076ff994c1a0f68`  
		Last Modified: Wed, 21 May 2025 23:49:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2f6b92592e3f57dbba3221b48b0dce566be344c3e646a89421cfc68ac2827925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857e0ef0a015c3e4c292fe0a24e960bbfba6c8f5844e8022a8d5c11a52d798c8`

```dockerfile
```

-	Layers:
	-	`sha256:7fb0e5e8b1ea53e4ba20b1cee752d37de3b49eaa2c057aea103fb67ad94a2cf5`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 2.3 MB (2311273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:210181bb919654e239b27e79e0a1003bde8ec7d3dd27841dfb0f95d0c62d23d4`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4fc35e2dfad1e5506199e79f54d5400afd22aee2bb1fe0b5e554d051c7c38d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32711358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d9217ce2913b829164781088c527a86fb1d43a48403bfd92c09a9ce7fd4c95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661e0135b0352aad675030e66bdddcf402a36cea02deb2532b0a24d5ba27554`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e7084e0aea669193e1cab086c096bd0764a05f1bf138e1f7c8f0c04eaf3b52`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.4 MB (2355810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259807b0c15878094bf0f3b13afedc0ef32d7eb679af66072ae18096127d72e1`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.3 MB (2288755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacab3ed6c99f53a622eefcda0dee8f57e377bfb97e7f57674e5030b7172988c`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12316079cc5378e29c63fc769e3686207ce41caec7ed76e8e5bb2c3e3b9a4938`  
		Last Modified: Thu, 22 May 2025 00:10:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:ed76bdc15573ee04e086b0a05bfe7056bb260ef0625d8fca2b4c89bd490db508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282362d3d316c5b5bd6b78ff5cfdd9be97d18c3c0018244eeac32f5a123b7d24`

```dockerfile
```

-	Layers:
	-	`sha256:f50a38ae76734a0eff8b24f4e99acd0d1bdb9ab848e04f9ddbcdcf08aadbe908`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.3 MB (2309305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ec44f0bfbd8d8065048e9d7bc8c90c0dcc460586efa613acacb43cb444f3c91`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 25.5 KB (25516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:427a7ad7f639e7cbf4161751cad9450044cbfaf6be8180abc51e01f68cad186c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33962949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a7e05a07d6b637c8752b13cee1ed7a5ebe2a4ef846c0eecaf4b7904d07ff4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d0594fdf9f07f23d90458a489d7972ab011bc5cca342af82850c3e9c024e3e`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4797e4e934c0c059a34c8b9d6c2adc40dece3f2ba61185edfa1c36591ef3549f`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.5 MB (2502658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7cc241a1440cfefd9f5b88cb6233b9ee820398da0c74155859c3114dd0646c`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.3 MB (2251292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cacd3ce01b0221992568e7179a1408774519b7dfbfc1daf37095764ae9bf16`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4abb18b4fabd731df2a3dbba62cd3f6de6cc4a6ab8419827bcbeb87641c4ad7`  
		Last Modified: Wed, 21 May 2025 23:16:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3c7de609f262a2ab1ddafedf272ac08f1eded0a2b08450f76dbd927b4b746f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfd69fc1ff5ceb8e449d8374c86427aafe41200a46c937aee60fce7a21ebf13`

```dockerfile
```

-	Layers:
	-	`sha256:87803ae24543fc1d1ecf0d1af68207e9714fd56829bab2354f9dd3940e3cf240`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.3 MB (2306133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b6feaf94b04b7737bdbf12b7c3f15ea0f7c46ead6614b9a46a82b87b5e5c75`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:55e7557e19928aa1991fbb59dcb75ea75b5b87115b772f36fd7302618c031468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32774540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1d55a83743e8701a5f0aacd60bd4260744537318e9335e6f681f765a2f536e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Wed, 21 May 2025 22:28:22 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00be87e076613598c61cb34d1eab1a04e74cb16c312c6b2737aaa5b2f54f0cad`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4fdba1c45e7b51399330c05d6b7e619f96cc0ed80cfd6bc75722cf5c982105`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 1.9 MB (1944079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d0d8b3f93dba36eb05fef21a3cda9faaf4e064e161fb87965839f9da4a2a20`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 2.3 MB (2317092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d4a6285da352b0857160c9194204e6801269736b4b18ca39bead26e9be8345`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d044aab1c575f4ebf7752dd0c9d988fc02e7b6f86316622b1678cea3cb9ca44`  
		Last Modified: Thu, 22 May 2025 00:11:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:048fdf15ee7c39e63ec03618e8587191e3915649f1b0076574f19773f9ccf067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c546fba658eb64c00d4036d1ac6c25e4a6f0b1681950c03a94ffc3954fb0d5c9`

```dockerfile
```

-	Layers:
	-	`sha256:2d39a6be744c7e579e7d4147fdc82a19956c6223fcb98601955e9a0a5d1e9e2e`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 25.2 KB (25216 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:3e871b866378795839b5bac555437a97646aa6f1c2abccdd182fe6b8ea84c983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37197690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9129b120bccf4a13f93ae0e47a4046e9ab94b4ff2d8de473eb248683b2802a6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Wed, 21 May 2025 22:28:16 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50fa062d3f9b2ead925a10e36e54327c0aae0c280d34e1075bcf82708310f13`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c345e70ea367cfeb023138dcae0d694e941f247957111430bd191f08181ef2b`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.7 MB (2710200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bd27f00915f27350ad09f9ca295e22cc787fe09c28db9040ad1bfcbfb1508d`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.4 MB (2419066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eee08866234c70e5aa7c719d396e45b9f8955b9a790d0654fd365d3c76c73d5`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0641a69e7e1f05a1544285cb3b709a8b9228ca6d1e6d96c66a0ae3f60cbc246f`  
		Last Modified: Wed, 21 May 2025 23:38:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:284c98dff5f2a0ad150bd4211a1db129fd87428ca2dde05427a3d4470d23d784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2338855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a8b8e6552c03d26ecc498bc8ff9ea559e55ea267d60e50335e46a93423df9`

```dockerfile
```

-	Layers:
	-	`sha256:529db81d9e88463a9e87c4177e55e182fb444bfc991ca4c30bab1e9cb81936e2`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.3 MB (2313462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b94ad3350b6fceb471a3b45c6d44ab4dfbfcbe1d28aeff91254919fe0cfdc04`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 25.4 KB (25393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.38-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:949a4a30fca21f6a731aafd862d71f8b49ba9a8499f7d5fee52e7dd0cc5481c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31304875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae677ba0b021f969e80917c5866c4ad53dc0c6406cf6c32e1453b0bab9152d77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2f122115cc85d695acc4bd6bce955e259f1bbad28dc671e212eaf4793195e7`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c30cebca59bfd8fbcc77d6107f2e1f0ee44ec402a34a0a31604aa524a390a1`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.2 MB (2156961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c2d1ec6d6a0ae48f133bf8b323c42f088f609830eba9aba813c3f613ce67e5`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.3 MB (2263596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085b757a938317b0432d2c6e577bb26b74869f14bdb090efd1e3108581b8acac`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f05beedc084a77558e99193cabc217fa002c1042529df98c5208f1d819d325`  
		Last Modified: Wed, 21 May 2025 23:28:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.38-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:25e3d5e4f2c4ca9668835e3673d0f663e4034016efbd9381b33ae2b961dd7d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e5415c88643fa263a323da5616aca4b27b38aab4197943da866f83fae75f84`

```dockerfile
```

-	Layers:
	-	`sha256:acc18fbdd9cb8d010d8ea1d191203d0c8e33ba9dce4fe255c1f8419cb63173e7`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.3 MB (2308704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa9690c26e582bfe6c776880fd91701c7a69b74e44fa78dd536af4fc3e871259`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:35090b653875831ecc957a7c16c0f582c2b92090100f74ae5ca70786f2c367ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
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

### `memcached:alpine` - linux; amd64

```console
$ docker pull memcached@sha256:90ff65aa470196afc5361ee16ebb344c3fb42f6317c16e4babaec1c79ad476ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5746542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c733c89a0ba90440ee956db059a3616a71a5e394c8dc9c9f6c1a9214b745d771`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3211cc8fb7612d73a250fd41e8ce1b264d4bafde9010ea586db45a946cb9dd79`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2692de63622aa06cd0ab32cbab5ebaac7c5c72f7f69c9c81711ec7196affb045`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 104.7 KB (104697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3694ff7984b804f1b2422eccdace864bc5b29564ff174a1e81f6b15ad9ad64e5`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 2.0 MB (1998247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a875c9e38db3d48eaf047d806f55e1ad705d891e17b24e691c6ae06b04416de`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d8aff7b7f4a9a5b7acb0870b99bc082dab792802823f42cb3df6bac425a03a`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:815522b8bf7a5c758712c55e2dfd2ba153f6d5def56049ebca9689c40b47036e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 KB (117423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e7d1adeedbeaad748f0fb03984aebb1f7b8d7a578733dfed68ae55a4d8aca5`

```dockerfile
```

-	Layers:
	-	`sha256:16f52c61ed51ca807453bbac564f16e1bc7438d019b75b43b432beee3917cf9e`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a618a61037789490baaad3bd81b36e771be572bc09db7bb521a4ea03c2c7199`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 23.8 KB (23790 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4d05de82436bd51ed609a745b8ddd01e296692beb5a372dcbdcf0b1f54818d03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4270486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e8bda6e6346ca01fa3a313ef7bcfcc696040d48be803f6c16922dedc8deae1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:44:25 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Dec 2020 01:44:29 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 17 Dec 2020 01:44:30 GMT
ENV MEMCACHED_VERSION=1.6.9
# Thu, 17 Dec 2020 01:44:31 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Thu, 17 Dec 2020 01:47:40 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Dec 2020 01:47:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Dec 2020 01:47:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Dec 2020 01:47:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:47:44 GMT
USER memcache
# Thu, 17 Dec 2020 01:47:45 GMT
EXPOSE 11211
# Thu, 17 Dec 2020 01:47:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc04af65958529b14246e2401008ef0186d74a33d2aa1b64d5f49633a1ff8f1`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bb28157acd02855bdf031eb7158f2cbb9849a6a9e6b45b4b82b507df6d83e9`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 14.9 KB (14904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b32778d38f805e0e2a84689dba047adda457098c6f4a0b3aeb51a9e9d3e7f2b`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 1.6 MB (1649753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506d15aa86681d1812c5696615302d2a50938410c852b6aa0d0680c7baa4589f`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55730e61cf75cdadfaf0682212c74d7a2355e652e0655cc74ba35a4b7cfb4c1`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull memcached@sha256:ac249cab7023411f8a5907f3a76e9ea920d08417bb843a490be5713136db3e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af971c76faaef52be66fc01361500e52479d9bd3de8c61e1ef111fba60d5dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f8cd16a2143448bb838f761683fc0d0414b211efd908c29739ea8fd5596ca`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ea935f106a5cac5c3db1cf082812746503193aad9a99f38a4b21f224a57e1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 120.8 KB (120773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63311bdf55b9f3cf77efa26b0da012e373d170b987229f428ce76b886bbce469`  
		Last Modified: Wed, 02 Apr 2025 00:26:44 GMT  
		Size: 2.0 MB (1989465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1d29b03fe2e901538845f42fc32d02e219b7ee32ae4e96d693d524c107f489`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bd8da7aa9a5f757c9aa94050d20b6125e7db478d3d09d066d7bacc647e82cd`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ad5f230ec532bb07cca752d58c44405687441c7cf07466de1abb8010fe83444b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 KB (117724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e862b1f07efa9790536488995533c7e658e410b55494d4f40578655c76e97e96`

```dockerfile
```

-	Layers:
	-	`sha256:2ae3d7cc25dc211d941164751cecdab1653e411fd74ac6d8792c5b3d72661cc4`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14ce594178b9c4afdf8d733cda3d894e4a9ad61c28d1ac8f7768f95d1c8f3b0b`  
		Last Modified: Wed, 02 Apr 2025 00:26:44 GMT  
		Size: 24.0 KB (23987 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:d4bdd5dcadda94a10fe78fdbf45d948bbfaa8233c6747b530c9e60319c7ba800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3154682685d8fd270595d40c1049cb408aed0282f2c747604db8442fcef5dfe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645c39e6b0ed26b821f36985348fb5422ae3b6196b7cf12ef50dda5a81d2b93`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4567ac7ea6d13e132381838b339c502058075a6fc0b18186ab1799070146919f`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 109.5 KB (109488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b78d96d6f34941f27c987768132a4c5c18ef33bd672132df7d9c5a820399226`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 2.0 MB (1959719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b507bd921881822a186cd02039a745dad142b6e8030ef7de46647172ec3830f`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5982dc98a348c1424c4189f2fc4e046ddfa92211012c880445f8c8f587fcc8`  
		Last Modified: Wed, 02 Apr 2025 00:02:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a8fcd0e85c073ee5e2cb2181ec295a8a17487566fd2c86ae081021eb5c246d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 KB (117320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b74d45db45f5c8f0ff0f375a08d4173e6d117f52c764d692162cc3c7ce2779`

```dockerfile
```

-	Layers:
	-	`sha256:200655427be8ca8fd2a9527ab234f19e1ae2927df5ae049b42f413365ecc92d9`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9ea6164d6c395a7b52b1395f9884889dd65a2f2aabf838e84561eeb87890b6c`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 23.7 KB (23732 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:846bb02f30ec4006d9b170f8e2fac3617b994e1d5ffbfcbd872c7d916523b4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022d4e1e17a86c0612d17c441ef3227d9042c46d5feecdd9c2a273b8314469e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81a068108debd592bc5100e24523483d0e5439f65b1c2eac8795522da51a6f0`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1b08fecb6beefd2da11b480a18e59255878a54a949bf6bfd470917dcafe91a`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aeecda3ee3acaf18a7673b403236cbe8d93f545f12bc55621b6f37e513900a5`  
		Last Modified: Wed, 02 Apr 2025 00:31:25 GMT  
		Size: 2.1 MB (2091349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b592e99d4871d2d634a039a4d058bed8d83febeccf5444e606b4420f0aa99c6`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c78b4428d40f07afd310ae82ed6fba84a4614528eb42ab1f92520bac7a191e0`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1656858c9dc9f1197d5b06660d09e4b57f90eed888dacf469ef312f4662e332b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 KB (115604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6a6900dce886d3fa69d25d431a1266fa1944b76e6ba8d139a5d00c0adaed75`

```dockerfile
```

-	Layers:
	-	`sha256:ec185783a159561468b1b9fadb3fd45605c017f8b76fb472b8202218447896c0`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:236149af7dac34fda2172de648c11f6afaa5c6e6566f2a909ad14f671f3c9008`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:b2d20d9478f0865295f104d69a10a6af47a42a19e0dce14f29edb38774033203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e583bfbee3cc9a94a7b502b1a173f9bf4111fca05ea1278df906891196781025`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf0ec129ec8a2b4d4a1c63ccbf427d2a09e4964506f173b2d50e16da5c5d85d`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87ff2734bb4c56d7bc73ec0ff994ec23d27330caef800d8833aabe135a40c16`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 107.9 KB (107853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efd9838e543fe84c79d3055949dc5f19a024e408550ed536f137c7c1d82dc49`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 1.9 MB (1932539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98def9beaf0eda5e2c72d1bb51c0ba6fd3c4fa353bd2ffaa71c769fc1e24e097`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ed44c8b9815cf9aebd7cb9e2526354718cbcda21e982ef1644179e23f3ed68`  
		Last Modified: Wed, 02 Apr 2025 02:42:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b79d62e7bee66523ce599bf19665532e58184f1418dcaa75319ae276df7e7102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 KB (115600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc405e5fbc58e4cbffe75922414fde14af323b70005eec6bd80a84057139b80`

```dockerfile
```

-	Layers:
	-	`sha256:f73a53dbdd9178f81244bf32411a1b2748d2a982b43a387ffa12e397da212ac3`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 91.7 KB (91736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41960c07a99d18bed2becce19308f78dbc107450842b1b59bdb2583336c463c8`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:3f70ed54bc6d6486a26fa5d844d30d158f78ee530a9b9ad92d9ee0165bbe3b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5620401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efb254b83b2d2bcf8ea4b50253aca87b5bc46f9f5593b6829b17550790a8f00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e7532ce01b9a31f1f3df73165c991b23b03e88dca43c46f5cc24237fc103d3`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff362c9247c7186b179ab36b3f74241e85aacd9e6bca6d4ef92adad9cfb9e2cd`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 113.5 KB (113461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8290f37bed0ef8feae03102a7631bc1d855099e839e088b703d3abbaf3883921`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 2.0 MB (2038025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b66de72a4b2ca75ad48d4f2e31e85116103f8e920c92abeebfcbe8a523bc048`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f9594fc6f70b3bc4eca62bf52dbc1accfd31976eef6d947935500066ec5a66`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6000519346e0e698f4e7b53de4fcdb0dc0a7295e922b1ddf5821c39083d85aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 KB (115471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c794c1f5316b791d894d4cb76365cfe77788960fbfb22ec98b8fc72b26bd0e3`

```dockerfile
```

-	Layers:
	-	`sha256:4df28bd3243c0b3247802e9fbda82c25885df47aeb6adc72737fa52615c9d38a`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbf6a1d4a771c26772accd7269d7279e63402148a1eda5a7d29db4ac1101662d`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 23.8 KB (23789 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.21`

```console
$ docker pull memcached@sha256:5ac71d3889701bd0750d35b06762ab7efc873ef29d7a43848ef5b0dc30a0dad4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
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

### `memcached:alpine3.21` - linux; amd64

```console
$ docker pull memcached@sha256:90ff65aa470196afc5361ee16ebb344c3fb42f6317c16e4babaec1c79ad476ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5746542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c733c89a0ba90440ee956db059a3616a71a5e394c8dc9c9f6c1a9214b745d771`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3211cc8fb7612d73a250fd41e8ce1b264d4bafde9010ea586db45a946cb9dd79`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2692de63622aa06cd0ab32cbab5ebaac7c5c72f7f69c9c81711ec7196affb045`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 104.7 KB (104697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3694ff7984b804f1b2422eccdace864bc5b29564ff174a1e81f6b15ad9ad64e5`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 2.0 MB (1998247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a875c9e38db3d48eaf047d806f55e1ad705d891e17b24e691c6ae06b04416de`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d8aff7b7f4a9a5b7acb0870b99bc082dab792802823f42cb3df6bac425a03a`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:815522b8bf7a5c758712c55e2dfd2ba153f6d5def56049ebca9689c40b47036e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 KB (117423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e7d1adeedbeaad748f0fb03984aebb1f7b8d7a578733dfed68ae55a4d8aca5`

```dockerfile
```

-	Layers:
	-	`sha256:16f52c61ed51ca807453bbac564f16e1bc7438d019b75b43b432beee3917cf9e`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 93.6 KB (93633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a618a61037789490baaad3bd81b36e771be572bc09db7bb521a4ea03c2c7199`  
		Last Modified: Wed, 02 Apr 2025 00:02:28 GMT  
		Size: 23.8 KB (23790 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ac249cab7023411f8a5907f3a76e9ea920d08417bb843a490be5713136db3e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af971c76faaef52be66fc01361500e52479d9bd3de8c61e1ef111fba60d5dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f8cd16a2143448bb838f761683fc0d0414b211efd908c29739ea8fd5596ca`  
		Last Modified: Thu, 20 Mar 2025 18:01:32 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ea935f106a5cac5c3db1cf082812746503193aad9a99f38a4b21f224a57e1`  
		Last Modified: Thu, 20 Mar 2025 18:01:33 GMT  
		Size: 120.8 KB (120773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63311bdf55b9f3cf77efa26b0da012e373d170b987229f428ce76b886bbce469`  
		Last Modified: Wed, 02 Apr 2025 00:26:44 GMT  
		Size: 2.0 MB (1989465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1d29b03fe2e901538845f42fc32d02e219b7ee32ae4e96d693d524c107f489`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bd8da7aa9a5f757c9aa94050d20b6125e7db478d3d09d066d7bacc647e82cd`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:ad5f230ec532bb07cca752d58c44405687441c7cf07466de1abb8010fe83444b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 KB (117724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e862b1f07efa9790536488995533c7e658e410b55494d4f40578655c76e97e96`

```dockerfile
```

-	Layers:
	-	`sha256:2ae3d7cc25dc211d941164751cecdab1653e411fd74ac6d8792c5b3d72661cc4`  
		Last Modified: Wed, 02 Apr 2025 00:26:43 GMT  
		Size: 93.7 KB (93737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14ce594178b9c4afdf8d733cda3d894e4a9ad61c28d1ac8f7768f95d1c8f3b0b`  
		Last Modified: Wed, 02 Apr 2025 00:26:44 GMT  
		Size: 24.0 KB (23987 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:d4bdd5dcadda94a10fe78fdbf45d948bbfaa8233c6747b530c9e60319c7ba800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3154682685d8fd270595d40c1049cb408aed0282f2c747604db8442fcef5dfe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645c39e6b0ed26b821f36985348fb5422ae3b6196b7cf12ef50dda5a81d2b93`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4567ac7ea6d13e132381838b339c502058075a6fc0b18186ab1799070146919f`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 109.5 KB (109488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b78d96d6f34941f27c987768132a4c5c18ef33bd672132df7d9c5a820399226`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 2.0 MB (1959719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b507bd921881822a186cd02039a745dad142b6e8030ef7de46647172ec3830f`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5982dc98a348c1424c4189f2fc4e046ddfa92211012c880445f8c8f587fcc8`  
		Last Modified: Wed, 02 Apr 2025 00:02:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:a8fcd0e85c073ee5e2cb2181ec295a8a17487566fd2c86ae081021eb5c246d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 KB (117320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b74d45db45f5c8f0ff0f375a08d4173e6d117f52c764d692162cc3c7ce2779`

```dockerfile
```

-	Layers:
	-	`sha256:200655427be8ca8fd2a9527ab234f19e1ae2927df5ae049b42f413365ecc92d9`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 93.6 KB (93588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9ea6164d6c395a7b52b1395f9884889dd65a2f2aabf838e84561eeb87890b6c`  
		Last Modified: Wed, 02 Apr 2025 00:02:53 GMT  
		Size: 23.7 KB (23732 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:846bb02f30ec4006d9b170f8e2fac3617b994e1d5ffbfcbd872c7d916523b4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022d4e1e17a86c0612d17c441ef3227d9042c46d5feecdd9c2a273b8314469e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81a068108debd592bc5100e24523483d0e5439f65b1c2eac8795522da51a6f0`  
		Last Modified: Thu, 20 Mar 2025 18:01:57 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1b08fecb6beefd2da11b480a18e59255878a54a949bf6bfd470917dcafe91a`  
		Last Modified: Thu, 20 Mar 2025 18:01:58 GMT  
		Size: 124.3 KB (124280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aeecda3ee3acaf18a7673b403236cbe8d93f545f12bc55621b6f37e513900a5`  
		Last Modified: Wed, 02 Apr 2025 00:31:25 GMT  
		Size: 2.1 MB (2091349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b592e99d4871d2d634a039a4d058bed8d83febeccf5444e606b4420f0aa99c6`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c78b4428d40f07afd310ae82ed6fba84a4614528eb42ab1f92520bac7a191e0`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:1656858c9dc9f1197d5b06660d09e4b57f90eed888dacf469ef312f4662e332b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 KB (115604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6a6900dce886d3fa69d25d431a1266fa1944b76e6ba8d139a5d00c0adaed75`

```dockerfile
```

-	Layers:
	-	`sha256:ec185783a159561468b1b9fadb3fd45605c017f8b76fb472b8202218447896c0`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 91.7 KB (91740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:236149af7dac34fda2172de648c11f6afaa5c6e6566f2a909ad14f671f3c9008`  
		Last Modified: Wed, 02 Apr 2025 00:31:24 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; riscv64

```console
$ docker pull memcached@sha256:b2d20d9478f0865295f104d69a10a6af47a42a19e0dce14f29edb38774033203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e583bfbee3cc9a94a7b502b1a173f9bf4111fca05ea1278df906891196781025`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf0ec129ec8a2b4d4a1c63ccbf427d2a09e4964506f173b2d50e16da5c5d85d`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87ff2734bb4c56d7bc73ec0ff994ec23d27330caef800d8833aabe135a40c16`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 107.9 KB (107853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efd9838e543fe84c79d3055949dc5f19a024e408550ed536f137c7c1d82dc49`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 1.9 MB (1932539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98def9beaf0eda5e2c72d1bb51c0ba6fd3c4fa353bd2ffaa71c769fc1e24e097`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ed44c8b9815cf9aebd7cb9e2526354718cbcda21e982ef1644179e23f3ed68`  
		Last Modified: Wed, 02 Apr 2025 02:42:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:b79d62e7bee66523ce599bf19665532e58184f1418dcaa75319ae276df7e7102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 KB (115600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc405e5fbc58e4cbffe75922414fde14af323b70005eec6bd80a84057139b80`

```dockerfile
```

-	Layers:
	-	`sha256:f73a53dbdd9178f81244bf32411a1b2748d2a982b43a387ffa12e397da212ac3`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 91.7 KB (91736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41960c07a99d18bed2becce19308f78dbc107450842b1b59bdb2583336c463c8`  
		Last Modified: Wed, 02 Apr 2025 02:42:42 GMT  
		Size: 23.9 KB (23864 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:3f70ed54bc6d6486a26fa5d844d30d158f78ee530a9b9ad92d9ee0165bbe3b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5620401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efb254b83b2d2bcf8ea4b50253aca87b5bc46f9f5593b6829b17550790a8f00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		patch 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e7532ce01b9a31f1f3df73165c991b23b03e88dca43c46f5cc24237fc103d3`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff362c9247c7186b179ab36b3f74241e85aacd9e6bca6d4ef92adad9cfb9e2cd`  
		Last Modified: Thu, 20 Mar 2025 18:06:38 GMT  
		Size: 113.5 KB (113461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8290f37bed0ef8feae03102a7631bc1d855099e839e088b703d3abbaf3883921`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 2.0 MB (2038025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b66de72a4b2ca75ad48d4f2e31e85116103f8e920c92abeebfcbe8a523bc048`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f9594fc6f70b3bc4eca62bf52dbc1accfd31976eef6d947935500066ec5a66`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:6000519346e0e698f4e7b53de4fcdb0dc0a7295e922b1ddf5821c39083d85aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 KB (115471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c794c1f5316b791d894d4cb76365cfe77788960fbfb22ec98b8fc72b26bd0e3`

```dockerfile
```

-	Layers:
	-	`sha256:4df28bd3243c0b3247802e9fbda82c25885df47aeb6adc72737fa52615c9d38a`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 91.7 KB (91682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbf6a1d4a771c26772accd7269d7279e63402148a1eda5a7d29db4ac1101662d`  
		Last Modified: Wed, 02 Apr 2025 00:52:13 GMT  
		Size: 23.8 KB (23789 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:0f92cdf1ca059c3b747f95328ed9e8de40866896657cb2b73148be36331efc02
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

### `memcached:bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:15c127398e9bb6bdfdbd6689b817964617401f2d9ca294758323011b3bb09350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33021901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f40f7fb4f0d5e586a146a0a994596292ea1e784ca1657eed1192b2fe17a003c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62639a9e53d980a0e86e3b54ae34e1e913a7f6cebd1bce7741e629047b732896`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5783d9aa8a04d558f9d1d5407d3f6dddb064b0a670738a5cbc480866bbc1a30`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.5 MB (2492219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609bfa774ee059a5d07cc14920af077ac7de9039c567f38164ea31f5eb04d3ba`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.3 MB (2302838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062ee789e2fd31345a9db851ddb0616c67ac7a4ea84e3a0e953af88faa98e3e5`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8416b27aabc571df320856a2ff533825bcbfc2fa602782561ff6b1a0449b821`  
		Last Modified: Wed, 21 May 2025 23:16:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7b5eaaa81772b0dc7377f0c8a8d41bb09c38c1a07292c0e0bef5654ceef3a28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c8287d2eb936f10093c74288a99d09a35c07df6033435ba68847dba2b0fdff`

```dockerfile
```

-	Layers:
	-	`sha256:f5c222a0451ee4a8115a7a9421176131c1481dd511e4ec028e050fdf94e7b741`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.3 MB (2308990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01ac10f70adef13c64045d3be5956b00caafe800e1fab7640f6eaa5f9ea66864`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:9d0d272209b7fd9922e4184de83ab429d527ad56c2f92a6a262cb88cf331551e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30087755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8113ec8739204304b1054312c93717e8c84189d23a003648ffa966d472462cad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01741d1d3bd96678d0f5dccb883892b5af0a3ffb6fe1abaf71cfa8d27579819`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e33674278ab7a59427b75a5c5a4fc74379bdc2cea1105e212becedfd13aadc`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.1 MB (2097064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c00b2be2834a255d33718d0903d2637ed005c981ee3d72a52654f7e0aed5e78`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.2 MB (2232281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148a70549f08f93b07f1c60ad72af807c88405d06687d9fe374648b9a484d40e`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93adc89552cc46d51abc366499a6fac900badfa05b8a0c8c604a7e4ac0cae40`  
		Last Modified: Wed, 21 May 2025 23:46:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7659c54d461b01b9e2062f0a8843b75b7d6a793c3d358a339b78e071770dcbd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2338302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af770cd911aab0856b542fdf7bc835ddf01b1ce26aa176b7b9cacfbc9388fb2d`

```dockerfile
```

-	Layers:
	-	`sha256:6d50a9e0dd879a75ce6c9396bd03c5ecb9beefd32a2d5bd6cf54f36341327685`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.3 MB (2312836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f3107fa09f2c0b66f32bebd5a1bb01208c84b9fa1da768bf5a5dbd20ca500d0`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v7

```console
$ docker pull memcached@sha256:95630a66e2d5c3a453ccc0f22d18ce0a297f1f21536938ff8f1b93c86b9cfbea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28065225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127e001dab188acb98ae7340be866c4c3ae686a9285cf40bd10f9dc702a73ee9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b5a50ba24d961f5862446c5e48fe0c5dbf9acfb0a3718255dd76fab71e84a7`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4adc063a4b96db7c50bcc78cd236a7102a3c31a61fb4216967b2cdcab50c24`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 1.9 MB (1946317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26fc15d35761b3f0c7797ea1ffc39ab51d4227089df7d6b5d2a075730795d20`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 2.2 MB (2184474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64f51527fd9673b0b39f52e4d608185f9461b4282e581e5ef1ce245bdc451e8`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138b4847c3beba31cf3c1807f17ce0b970ec15f04604f92ac076ff994c1a0f68`  
		Last Modified: Wed, 21 May 2025 23:49:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2f6b92592e3f57dbba3221b48b0dce566be344c3e646a89421cfc68ac2827925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857e0ef0a015c3e4c292fe0a24e960bbfba6c8f5844e8022a8d5c11a52d798c8`

```dockerfile
```

-	Layers:
	-	`sha256:7fb0e5e8b1ea53e4ba20b1cee752d37de3b49eaa2c057aea103fb67ad94a2cf5`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 2.3 MB (2311273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:210181bb919654e239b27e79e0a1003bde8ec7d3dd27841dfb0f95d0c62d23d4`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4fc35e2dfad1e5506199e79f54d5400afd22aee2bb1fe0b5e554d051c7c38d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32711358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d9217ce2913b829164781088c527a86fb1d43a48403bfd92c09a9ce7fd4c95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661e0135b0352aad675030e66bdddcf402a36cea02deb2532b0a24d5ba27554`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e7084e0aea669193e1cab086c096bd0764a05f1bf138e1f7c8f0c04eaf3b52`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.4 MB (2355810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259807b0c15878094bf0f3b13afedc0ef32d7eb679af66072ae18096127d72e1`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.3 MB (2288755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacab3ed6c99f53a622eefcda0dee8f57e377bfb97e7f57674e5030b7172988c`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12316079cc5378e29c63fc769e3686207ce41caec7ed76e8e5bb2c3e3b9a4938`  
		Last Modified: Thu, 22 May 2025 00:10:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:ed76bdc15573ee04e086b0a05bfe7056bb260ef0625d8fca2b4c89bd490db508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282362d3d316c5b5bd6b78ff5cfdd9be97d18c3c0018244eeac32f5a123b7d24`

```dockerfile
```

-	Layers:
	-	`sha256:f50a38ae76734a0eff8b24f4e99acd0d1bdb9ab848e04f9ddbcdcf08aadbe908`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.3 MB (2309305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ec44f0bfbd8d8065048e9d7bc8c90c0dcc460586efa613acacb43cb444f3c91`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 25.5 KB (25516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:427a7ad7f639e7cbf4161751cad9450044cbfaf6be8180abc51e01f68cad186c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33962949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a7e05a07d6b637c8752b13cee1ed7a5ebe2a4ef846c0eecaf4b7904d07ff4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d0594fdf9f07f23d90458a489d7972ab011bc5cca342af82850c3e9c024e3e`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4797e4e934c0c059a34c8b9d6c2adc40dece3f2ba61185edfa1c36591ef3549f`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.5 MB (2502658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7cc241a1440cfefd9f5b88cb6233b9ee820398da0c74155859c3114dd0646c`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.3 MB (2251292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cacd3ce01b0221992568e7179a1408774519b7dfbfc1daf37095764ae9bf16`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4abb18b4fabd731df2a3dbba62cd3f6de6cc4a6ab8419827bcbeb87641c4ad7`  
		Last Modified: Wed, 21 May 2025 23:16:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3c7de609f262a2ab1ddafedf272ac08f1eded0a2b08450f76dbd927b4b746f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfd69fc1ff5ceb8e449d8374c86427aafe41200a46c937aee60fce7a21ebf13`

```dockerfile
```

-	Layers:
	-	`sha256:87803ae24543fc1d1ecf0d1af68207e9714fd56829bab2354f9dd3940e3cf240`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.3 MB (2306133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b6feaf94b04b7737bdbf12b7c3f15ea0f7c46ead6614b9a46a82b87b5e5c75`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:55e7557e19928aa1991fbb59dcb75ea75b5b87115b772f36fd7302618c031468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32774540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1d55a83743e8701a5f0aacd60bd4260744537318e9335e6f681f765a2f536e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Wed, 21 May 2025 22:28:22 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00be87e076613598c61cb34d1eab1a04e74cb16c312c6b2737aaa5b2f54f0cad`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4fdba1c45e7b51399330c05d6b7e619f96cc0ed80cfd6bc75722cf5c982105`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 1.9 MB (1944079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d0d8b3f93dba36eb05fef21a3cda9faaf4e064e161fb87965839f9da4a2a20`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 2.3 MB (2317092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d4a6285da352b0857160c9194204e6801269736b4b18ca39bead26e9be8345`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d044aab1c575f4ebf7752dd0c9d988fc02e7b6f86316622b1678cea3cb9ca44`  
		Last Modified: Thu, 22 May 2025 00:11:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:048fdf15ee7c39e63ec03618e8587191e3915649f1b0076574f19773f9ccf067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c546fba658eb64c00d4036d1ac6c25e4a6f0b1681950c03a94ffc3954fb0d5c9`

```dockerfile
```

-	Layers:
	-	`sha256:2d39a6be744c7e579e7d4147fdc82a19956c6223fcb98601955e9a0a5d1e9e2e`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 25.2 KB (25216 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:3e871b866378795839b5bac555437a97646aa6f1c2abccdd182fe6b8ea84c983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37197690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9129b120bccf4a13f93ae0e47a4046e9ab94b4ff2d8de473eb248683b2802a6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Wed, 21 May 2025 22:28:16 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50fa062d3f9b2ead925a10e36e54327c0aae0c280d34e1075bcf82708310f13`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c345e70ea367cfeb023138dcae0d694e941f247957111430bd191f08181ef2b`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.7 MB (2710200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bd27f00915f27350ad09f9ca295e22cc787fe09c28db9040ad1bfcbfb1508d`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.4 MB (2419066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eee08866234c70e5aa7c719d396e45b9f8955b9a790d0654fd365d3c76c73d5`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0641a69e7e1f05a1544285cb3b709a8b9228ca6d1e6d96c66a0ae3f60cbc246f`  
		Last Modified: Wed, 21 May 2025 23:38:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:284c98dff5f2a0ad150bd4211a1db129fd87428ca2dde05427a3d4470d23d784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2338855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a8b8e6552c03d26ecc498bc8ff9ea559e55ea267d60e50335e46a93423df9`

```dockerfile
```

-	Layers:
	-	`sha256:529db81d9e88463a9e87c4177e55e182fb444bfc991ca4c30bab1e9cb81936e2`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.3 MB (2313462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b94ad3350b6fceb471a3b45c6d44ab4dfbfcbe1d28aeff91254919fe0cfdc04`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 25.4 KB (25393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:949a4a30fca21f6a731aafd862d71f8b49ba9a8499f7d5fee52e7dd0cc5481c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31304875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae677ba0b021f969e80917c5866c4ad53dc0c6406cf6c32e1453b0bab9152d77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2f122115cc85d695acc4bd6bce955e259f1bbad28dc671e212eaf4793195e7`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c30cebca59bfd8fbcc77d6107f2e1f0ee44ec402a34a0a31604aa524a390a1`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.2 MB (2156961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c2d1ec6d6a0ae48f133bf8b323c42f088f609830eba9aba813c3f613ce67e5`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.3 MB (2263596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085b757a938317b0432d2c6e577bb26b74869f14bdb090efd1e3108581b8acac`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f05beedc084a77558e99193cabc217fa002c1042529df98c5208f1d819d325`  
		Last Modified: Wed, 21 May 2025 23:28:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:25e3d5e4f2c4ca9668835e3673d0f663e4034016efbd9381b33ae2b961dd7d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e5415c88643fa263a323da5616aca4b27b38aab4197943da866f83fae75f84`

```dockerfile
```

-	Layers:
	-	`sha256:acc18fbdd9cb8d010d8ea1d191203d0c8e33ba9dce4fe255c1f8419cb63173e7`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.3 MB (2308704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa9690c26e582bfe6c776880fd91701c7a69b74e44fa78dd536af4fc3e871259`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:0f92cdf1ca059c3b747f95328ed9e8de40866896657cb2b73148be36331efc02
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

### `memcached:latest` - linux; amd64

```console
$ docker pull memcached@sha256:15c127398e9bb6bdfdbd6689b817964617401f2d9ca294758323011b3bb09350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33021901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f40f7fb4f0d5e586a146a0a994596292ea1e784ca1657eed1192b2fe17a003c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62639a9e53d980a0e86e3b54ae34e1e913a7f6cebd1bce7741e629047b732896`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5783d9aa8a04d558f9d1d5407d3f6dddb064b0a670738a5cbc480866bbc1a30`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.5 MB (2492219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609bfa774ee059a5d07cc14920af077ac7de9039c567f38164ea31f5eb04d3ba`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.3 MB (2302838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062ee789e2fd31345a9db851ddb0616c67ac7a4ea84e3a0e953af88faa98e3e5`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8416b27aabc571df320856a2ff533825bcbfc2fa602782561ff6b1a0449b821`  
		Last Modified: Wed, 21 May 2025 23:16:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:7b5eaaa81772b0dc7377f0c8a8d41bb09c38c1a07292c0e0bef5654ceef3a28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c8287d2eb936f10093c74288a99d09a35c07df6033435ba68847dba2b0fdff`

```dockerfile
```

-	Layers:
	-	`sha256:f5c222a0451ee4a8115a7a9421176131c1481dd511e4ec028e050fdf94e7b741`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 2.3 MB (2308990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01ac10f70adef13c64045d3be5956b00caafe800e1fab7640f6eaa5f9ea66864`  
		Last Modified: Wed, 21 May 2025 23:16:35 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:9d0d272209b7fd9922e4184de83ab429d527ad56c2f92a6a262cb88cf331551e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30087755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8113ec8739204304b1054312c93717e8c84189d23a003648ffa966d472462cad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01741d1d3bd96678d0f5dccb883892b5af0a3ffb6fe1abaf71cfa8d27579819`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e33674278ab7a59427b75a5c5a4fc74379bdc2cea1105e212becedfd13aadc`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.1 MB (2097064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c00b2be2834a255d33718d0903d2637ed005c981ee3d72a52654f7e0aed5e78`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.2 MB (2232281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148a70549f08f93b07f1c60ad72af807c88405d06687d9fe374648b9a484d40e`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93adc89552cc46d51abc366499a6fac900badfa05b8a0c8c604a7e4ac0cae40`  
		Last Modified: Wed, 21 May 2025 23:46:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:7659c54d461b01b9e2062f0a8843b75b7d6a793c3d358a339b78e071770dcbd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2338302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af770cd911aab0856b542fdf7bc835ddf01b1ce26aa176b7b9cacfbc9388fb2d`

```dockerfile
```

-	Layers:
	-	`sha256:6d50a9e0dd879a75ce6c9396bd03c5ecb9beefd32a2d5bd6cf54f36341327685`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 2.3 MB (2312836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f3107fa09f2c0b66f32bebd5a1bb01208c84b9fa1da768bf5a5dbd20ca500d0`  
		Last Modified: Wed, 21 May 2025 23:46:13 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:95630a66e2d5c3a453ccc0f22d18ce0a297f1f21536938ff8f1b93c86b9cfbea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28065225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127e001dab188acb98ae7340be866c4c3ae686a9285cf40bd10f9dc702a73ee9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b5a50ba24d961f5862446c5e48fe0c5dbf9acfb0a3718255dd76fab71e84a7`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4adc063a4b96db7c50bcc78cd236a7102a3c31a61fb4216967b2cdcab50c24`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 1.9 MB (1946317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26fc15d35761b3f0c7797ea1ffc39ab51d4227089df7d6b5d2a075730795d20`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 2.2 MB (2184474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64f51527fd9673b0b39f52e4d608185f9461b4282e581e5ef1ce245bdc451e8`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138b4847c3beba31cf3c1807f17ce0b970ec15f04604f92ac076ff994c1a0f68`  
		Last Modified: Wed, 21 May 2025 23:49:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:2f6b92592e3f57dbba3221b48b0dce566be344c3e646a89421cfc68ac2827925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857e0ef0a015c3e4c292fe0a24e960bbfba6c8f5844e8022a8d5c11a52d798c8`

```dockerfile
```

-	Layers:
	-	`sha256:7fb0e5e8b1ea53e4ba20b1cee752d37de3b49eaa2c057aea103fb67ad94a2cf5`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 2.3 MB (2311273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:210181bb919654e239b27e79e0a1003bde8ec7d3dd27841dfb0f95d0c62d23d4`  
		Last Modified: Wed, 21 May 2025 23:49:57 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:4fc35e2dfad1e5506199e79f54d5400afd22aee2bb1fe0b5e554d051c7c38d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32711358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d9217ce2913b829164781088c527a86fb1d43a48403bfd92c09a9ce7fd4c95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661e0135b0352aad675030e66bdddcf402a36cea02deb2532b0a24d5ba27554`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e7084e0aea669193e1cab086c096bd0764a05f1bf138e1f7c8f0c04eaf3b52`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.4 MB (2355810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259807b0c15878094bf0f3b13afedc0ef32d7eb679af66072ae18096127d72e1`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.3 MB (2288755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacab3ed6c99f53a622eefcda0dee8f57e377bfb97e7f57674e5030b7172988c`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12316079cc5378e29c63fc769e3686207ce41caec7ed76e8e5bb2c3e3b9a4938`  
		Last Modified: Thu, 22 May 2025 00:10:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:ed76bdc15573ee04e086b0a05bfe7056bb260ef0625d8fca2b4c89bd490db508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282362d3d316c5b5bd6b78ff5cfdd9be97d18c3c0018244eeac32f5a123b7d24`

```dockerfile
```

-	Layers:
	-	`sha256:f50a38ae76734a0eff8b24f4e99acd0d1bdb9ab848e04f9ddbcdcf08aadbe908`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 2.3 MB (2309305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ec44f0bfbd8d8065048e9d7bc8c90c0dcc460586efa613acacb43cb444f3c91`  
		Last Modified: Thu, 22 May 2025 00:10:58 GMT  
		Size: 25.5 KB (25516 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:427a7ad7f639e7cbf4161751cad9450044cbfaf6be8180abc51e01f68cad186c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33962949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a7e05a07d6b637c8752b13cee1ed7a5ebe2a4ef846c0eecaf4b7904d07ff4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d0594fdf9f07f23d90458a489d7972ab011bc5cca342af82850c3e9c024e3e`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4797e4e934c0c059a34c8b9d6c2adc40dece3f2ba61185edfa1c36591ef3549f`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.5 MB (2502658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7cc241a1440cfefd9f5b88cb6233b9ee820398da0c74155859c3114dd0646c`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.3 MB (2251292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cacd3ce01b0221992568e7179a1408774519b7dfbfc1daf37095764ae9bf16`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4abb18b4fabd731df2a3dbba62cd3f6de6cc4a6ab8419827bcbeb87641c4ad7`  
		Last Modified: Wed, 21 May 2025 23:16:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:3c7de609f262a2ab1ddafedf272ac08f1eded0a2b08450f76dbd927b4b746f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfd69fc1ff5ceb8e449d8374c86427aafe41200a46c937aee60fce7a21ebf13`

```dockerfile
```

-	Layers:
	-	`sha256:87803ae24543fc1d1ecf0d1af68207e9714fd56829bab2354f9dd3940e3cf240`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 2.3 MB (2306133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b6feaf94b04b7737bdbf12b7c3f15ea0f7c46ead6614b9a46a82b87b5e5c75`  
		Last Modified: Wed, 21 May 2025 23:16:16 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:55e7557e19928aa1991fbb59dcb75ea75b5b87115b772f36fd7302618c031468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32774540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1d55a83743e8701a5f0aacd60bd4260744537318e9335e6f681f765a2f536e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Wed, 21 May 2025 22:28:22 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00be87e076613598c61cb34d1eab1a04e74cb16c312c6b2737aaa5b2f54f0cad`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4fdba1c45e7b51399330c05d6b7e619f96cc0ed80cfd6bc75722cf5c982105`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 1.9 MB (1944079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d0d8b3f93dba36eb05fef21a3cda9faaf4e064e161fb87965839f9da4a2a20`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 2.3 MB (2317092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d4a6285da352b0857160c9194204e6801269736b4b18ca39bead26e9be8345`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d044aab1c575f4ebf7752dd0c9d988fc02e7b6f86316622b1678cea3cb9ca44`  
		Last Modified: Thu, 22 May 2025 00:11:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:048fdf15ee7c39e63ec03618e8587191e3915649f1b0076574f19773f9ccf067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c546fba658eb64c00d4036d1ac6c25e4a6f0b1681950c03a94ffc3954fb0d5c9`

```dockerfile
```

-	Layers:
	-	`sha256:2d39a6be744c7e579e7d4147fdc82a19956c6223fcb98601955e9a0a5d1e9e2e`  
		Last Modified: Thu, 22 May 2025 00:11:30 GMT  
		Size: 25.2 KB (25216 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:3e871b866378795839b5bac555437a97646aa6f1c2abccdd182fe6b8ea84c983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37197690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9129b120bccf4a13f93ae0e47a4046e9ab94b4ff2d8de473eb248683b2802a6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Wed, 21 May 2025 22:28:16 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50fa062d3f9b2ead925a10e36e54327c0aae0c280d34e1075bcf82708310f13`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c345e70ea367cfeb023138dcae0d694e941f247957111430bd191f08181ef2b`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.7 MB (2710200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bd27f00915f27350ad09f9ca295e22cc787fe09c28db9040ad1bfcbfb1508d`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.4 MB (2419066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eee08866234c70e5aa7c719d396e45b9f8955b9a790d0654fd365d3c76c73d5`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0641a69e7e1f05a1544285cb3b709a8b9228ca6d1e6d96c66a0ae3f60cbc246f`  
		Last Modified: Wed, 21 May 2025 23:38:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:284c98dff5f2a0ad150bd4211a1db129fd87428ca2dde05427a3d4470d23d784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2338855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a8b8e6552c03d26ecc498bc8ff9ea559e55ea267d60e50335e46a93423df9`

```dockerfile
```

-	Layers:
	-	`sha256:529db81d9e88463a9e87c4177e55e182fb444bfc991ca4c30bab1e9cb81936e2`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 2.3 MB (2313462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b94ad3350b6fceb471a3b45c6d44ab4dfbfcbe1d28aeff91254919fe0cfdc04`  
		Last Modified: Wed, 21 May 2025 23:38:16 GMT  
		Size: 25.4 KB (25393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:949a4a30fca21f6a731aafd862d71f8b49ba9a8499f7d5fee52e7dd0cc5481c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31304875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae677ba0b021f969e80917c5866c4ad53dc0c6406cf6c32e1453b0bab9152d77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 01 Apr 2025 23:49:01 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 01 Apr 2025 23:49:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/memcached/memcached/commit/1a0a0b2591176a7c82412e27f3e17ba9133cd8dd.patch?full_index=1'; 	echo '12441b94e0c35e2bd4511d10b799b731f3aae7428f196d34eccefb68351ed0f0 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		wget -O memcached-extstore-test-stability.patch 'https://github.com/memcached/memcached/commit/a2e47b5afdf6ad7deeb54ce9fb1d45cf8cfd1024.patch?full_index=1'; 	echo 'a421465488e2ffac5fe3d956598f030f5b06399af3dbb4e36ecebdd368245b4b *memcached-extstore-test-stability.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-extstore-test-stability.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-extstore-test-stability.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 01 Apr 2025 23:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 23:49:01 GMT
USER memcache
# Tue, 01 Apr 2025 23:49:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 01 Apr 2025 23:49:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2f122115cc85d695acc4bd6bce955e259f1bbad28dc671e212eaf4793195e7`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c30cebca59bfd8fbcc77d6107f2e1f0ee44ec402a34a0a31604aa524a390a1`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.2 MB (2156961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c2d1ec6d6a0ae48f133bf8b323c42f088f609830eba9aba813c3f613ce67e5`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.3 MB (2263596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085b757a938317b0432d2c6e577bb26b74869f14bdb090efd1e3108581b8acac`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f05beedc084a77558e99193cabc217fa002c1042529df98c5208f1d819d325`  
		Last Modified: Wed, 21 May 2025 23:28:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:25e3d5e4f2c4ca9668835e3673d0f663e4034016efbd9381b33ae2b961dd7d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e5415c88643fa263a323da5616aca4b27b38aab4197943da866f83fae75f84`

```dockerfile
```

-	Layers:
	-	`sha256:acc18fbdd9cb8d010d8ea1d191203d0c8e33ba9dce4fe255c1f8419cb63173e7`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 2.3 MB (2308704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa9690c26e582bfe6c776880fd91701c7a69b74e44fa78dd536af4fc3e871259`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json
