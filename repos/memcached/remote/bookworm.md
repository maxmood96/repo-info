## `memcached:bookworm`

```console
$ docker pull memcached@sha256:356e556d072787a987500f99bf27d22c31240baa73a1cf36a875b062e85927f3
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
$ docker pull memcached@sha256:a2bb21b8ffab89e082d59a61a1f7a9d0e86017ba3b8931066fc0da932bde8e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32712297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ce5bf4870889adb04c76539eacfa61c44182e56dfe36d4bb4f9a10949e154f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9e6b8fdf4f9e38c7fa898ea9599f02bec7e27e337841a778ee595718c7ec37`  
		Last Modified: Mon, 28 Apr 2025 22:38:17 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71440bc4d7292a79eabfaa7a725678c74aaf0d5cd90594ef1811d17420bd406b`  
		Last Modified: Mon, 28 Apr 2025 22:38:17 GMT  
		Size: 2.4 MB (2355383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9d1b21e519a12b304c8080fe54f81efaeaaaea3362c0e9634aa60ea7b3a2bd`  
		Last Modified: Mon, 28 Apr 2025 22:38:17 GMT  
		Size: 2.3 MB (2288783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5790b16ab8e64895ae3a944c6673e2e2aa5d1179f9541f8c2a5f0da3c68b88`  
		Last Modified: Mon, 28 Apr 2025 22:38:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa8ae9e08853ef84c2c372e3f8eb59f2726d2157a981d0e93c4aeec6f6b5d9a`  
		Last Modified: Mon, 28 Apr 2025 22:38:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:6f23759cb46e5498b11e042034502966cc778ea2e14204bc5c2ef79188f01456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b4e455e22fc651894d6629fd15d58f54259d6230b7cc07470ce3f756f68a91`

```dockerfile
```

-	Layers:
	-	`sha256:58cad89ce903f24b6e34a5d5aca4ad53fcc46a56da3a695645d272a29f2f5fa6`  
		Last Modified: Mon, 28 Apr 2025 22:38:17 GMT  
		Size: 2.3 MB (2290984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ccdde73c96201d86daeff351c76ff740ff24600a855423eed0241fb4034613c`  
		Last Modified: Mon, 28 Apr 2025 22:38:17 GMT  
		Size: 25.5 KB (25517 bytes)  
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
$ docker pull memcached@sha256:625ab26d1794f6088ddc8e02bd11cef2dabc6f5e021f419bb930d1d40bf5669e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32775951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8647f5344a2bdf26546f652686e9eb01970e3d8303af3fdd39c06aab20c3c96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1745798400'
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
	-	`sha256:901060d913f9d0bbb82847b3b60c3a263ed0dac4f75aa29161be6ed89b57082a`  
		Last Modified: Mon, 28 Apr 2025 21:11:19 GMT  
		Size: 28.5 MB (28514138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52c0280fb9a59d19120bfe4501aa31daaa5ac7e4fbf4c9a025afa4a691a30c6`  
		Last Modified: Mon, 28 Apr 2025 22:43:03 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4be0db129b99a99c33fddd39531b79d8e6acdae55c6e02ec6a47cb9f8a68c3`  
		Last Modified: Mon, 28 Apr 2025 22:43:03 GMT  
		Size: 1.9 MB (1943246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b364a4ea8d5b34e5d56798be47854a75430adce5d10ea6c224ae565688b0c75e`  
		Last Modified: Mon, 28 Apr 2025 22:43:03 GMT  
		Size: 2.3 MB (2317055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c49e85a634ca34d0ce215b60d46fb406ce011ea6200b07bc1321420d4cee5d`  
		Last Modified: Mon, 28 Apr 2025 22:43:03 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce89267cd3719559453e9a1dd5fab9bc7a552a0443abfb1c831beeededae766`  
		Last Modified: Mon, 28 Apr 2025 22:43:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:332fb96af7af711ed0ed6fa17c3f4a369b291e5f28a1a89216ed8a921cb1625c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa62a6d1a67a93083861fc0dc7e20eed9f8aac0d5f0e21b03aec107f494b107a`

```dockerfile
```

-	Layers:
	-	`sha256:f94bca6992bf758f34a36704843c06dbe1b8095613ebc2def08bfd8686e633d8`  
		Last Modified: Mon, 28 Apr 2025 22:43:02 GMT  
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
