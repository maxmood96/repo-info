## `memcached:latest`

```console
$ docker pull memcached@sha256:9e9f3552a5a42058c9138ce66e61f9b3e0737e17122c461ab3d004e5556a2129
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
$ docker pull memcached@sha256:0bcc95407b9d7690fe411bc1a32282126d69549e18c7435569e504fd1dbf8620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33026694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e935ede11459568409bb1bcc19e13ab4050fd5c6d13a524334ee556575b1f58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bdfce73326b4cc16bedf50bad6526519c61c5ea650fc0abaff89140de4987a`  
		Last Modified: Tue, 01 Jul 2025 02:16:57 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18141cd5ffc6960e5d97e4849d942d62341f72ee4dc860234653fbe38af30171`  
		Last Modified: Tue, 01 Jul 2025 02:16:57 GMT  
		Size: 2.5 MB (2492207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a943e6c69f606bb3f0ad57111cf7859cd7bcf55ab24565161acd15cbc29aaa`  
		Last Modified: Tue, 01 Jul 2025 02:16:58 GMT  
		Size: 2.3 MB (2302830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6420d9705c6d7bc731ccbd52dd8412158b69974cdb96991bd181807b0449a6a4`  
		Last Modified: Tue, 01 Jul 2025 02:16:57 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09010e5feb057a092cb3009a714c3505f22bd54d0a53616a12a2ad80bd2f598`  
		Last Modified: Tue, 01 Jul 2025 02:16:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:85b40828016259a5c3a6ac2daae4360f13ba3909c1a6e817c03d74b5299d97ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae6b3de76bd7d8c68c79e19724519155bbaa4a69929c41fbaa4bc3814785d6c`

```dockerfile
```

-	Layers:
	-	`sha256:537117d8c1485b0f47fb9205f0ec797be18e17cd28a43809d929e4ed883b08c1`  
		Last Modified: Tue, 01 Jul 2025 06:34:27 GMT  
		Size: 2.4 MB (2399984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7356362d9655cea16c35ba4c201361967435478246fa582111b5b6a1cd4cb1db`  
		Last Modified: Tue, 01 Jul 2025 06:34:29 GMT  
		Size: 25.3 KB (25319 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:4f6ba7cd80f3e9e8ac54dc35ff01a4a793bce45dfddf326bce157029c5fe7127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30093315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84c24ab05f195e5cb280f3bb2b14ae3939c22d2db61bce1d9202d36911861b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
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
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e3ae737339d80a524786546a2f1f626eeb8f3816c66ab0ed936ec5e1a6dde5`  
		Last Modified: Tue, 01 Jul 2025 02:47:40 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2406836deff96ca7650185e981cf865e029c08c9dae66f108020786334a1d7c8`  
		Last Modified: Tue, 01 Jul 2025 02:47:47 GMT  
		Size: 2.1 MB (2097052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3916b1e0998d2bd4bb060e385291fb351b7414d582b7991955e805c7b6dce0f`  
		Last Modified: Tue, 01 Jul 2025 02:47:47 GMT  
		Size: 2.2 MB (2232291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1f530319d3e6df61d345735794126424048dd59f38b7b8f448389e4e7ba780`  
		Last Modified: Tue, 01 Jul 2025 02:47:40 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859e173669e5645fafe1157b662c46c8dc9f71b551eb0fa76bb7c998e00aae21`  
		Last Modified: Tue, 01 Jul 2025 02:47:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:3726d1081e3be07480cce6a609cf475a567a54b40ee464fdbdcca75bf236d884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8259da4c299c42c69c1d357efa60e96303d45b4ce647ef9999f85894158356`

```dockerfile
```

-	Layers:
	-	`sha256:7b49df8a318a969590a42da3faab72d0612528ce2dfc0f1368fcbe3a2dd3c683`  
		Last Modified: Tue, 01 Jul 2025 03:34:35 GMT  
		Size: 2.4 MB (2403830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f27931577575ca562afeef1e56dab0d0c5e2a8a7e822d8706c5150f0d18f794e`  
		Last Modified: Tue, 01 Jul 2025 03:34:36 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:47360b31f3b3a7151610436a6cd391e2e7ade3131a406a58976746c2d2815818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28071070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dcc873f120690cc75a090cbad26436c15952d5215cc4db38142fbd530712dcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
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
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395e4f495582e6f798873b91769885b555dcb751765de8758f2754e356e39710`  
		Last Modified: Tue, 01 Jul 2025 05:13:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9a15c8e0a58e308e9df418af791dcab1891402129d79c4a43ce8c8347162b1`  
		Last Modified: Tue, 01 Jul 2025 05:13:54 GMT  
		Size: 1.9 MB (1946306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fc0d8484ef7600c21cc8d326b02e1ac0749226606541dc2521b7c03b48be76`  
		Last Modified: Tue, 01 Jul 2025 05:13:54 GMT  
		Size: 2.2 MB (2184506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd107fe2adbb97c7d699e423ee7365eafd9219094e3154d56e3ca71f6c7928e`  
		Last Modified: Tue, 01 Jul 2025 05:13:53 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015e21ab3de7de228a4f019b58061f03fb3318495f2e0f53b38bc138e2760271`  
		Last Modified: Tue, 01 Jul 2025 05:13:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:4b0c424f29596dc9b4b9d44f32eb484b1a40bf58a7aac2f1231d6e023808f070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2427734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a6803f87b12a3acae842639a0281ab3d94c326d19f107366b63c7f3d5df3cd`

```dockerfile
```

-	Layers:
	-	`sha256:be25daddf8e83daf45b3682081e92f2431cacd9fe8c14324bad51ca400229198`  
		Last Modified: Tue, 01 Jul 2025 06:34:36 GMT  
		Size: 2.4 MB (2402267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f404890f4faddd4ffd79b9ed213a1f146af8f5b5663b3f8efb911a6ad45817b`  
		Last Modified: Tue, 01 Jul 2025 06:34:37 GMT  
		Size: 25.5 KB (25467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:45a6bd824f96ab6e7903735e0585cf6c7fca78d6a4a4ac63c857d613895d0aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32723781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a726712e28fde35d5c893a07331ef56d8c2d9a3c174e68dbb50e4fcbe91947`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f1153f002c210547e923abac30cda2095f3ae2929b646135b94fff0cc8a908`  
		Last Modified: Tue, 01 Jul 2025 03:10:33 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37df509990a55f207b07ab337093d977d89a1850500efdd64a2f877203d694e2`  
		Last Modified: Tue, 01 Jul 2025 03:10:34 GMT  
		Size: 2.4 MB (2355808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6297eb4aeaa493d8b5cff723c786f6b22623128c1ed174a8eaadfb83777da85`  
		Last Modified: Tue, 01 Jul 2025 03:10:34 GMT  
		Size: 2.3 MB (2288781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a7eda5ec01c9cbc63a34dc39a14f56fcabe7bfb92733373b7d254be78ef5d4`  
		Last Modified: Tue, 01 Jul 2025 03:10:34 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f003f6f82c0df75cfa23c57dbf5ae14da8a28c71f1d3db3980c3287d41ce27b`  
		Last Modified: Tue, 01 Jul 2025 03:10:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:924c3e810eaa46e6cbbaebd04188d4d65186128020eb12f0eab36b9e3f64c293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:648c43a781aa63c94f99fe998b325926048fd18137117760f06a2c8a7ff00eb3`

```dockerfile
```

-	Layers:
	-	`sha256:b7246830d56fc7f3b7e34df3b2568ca892c220d0b0cac5f047a64943db643b5f`  
		Last Modified: Tue, 01 Jul 2025 03:34:42 GMT  
		Size: 2.4 MB (2400299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f773db0913fea7a9a4dfc72d2a2a9fdc758893183e24b888b926e9c16cf4210`  
		Last Modified: Tue, 01 Jul 2025 03:34:43 GMT  
		Size: 25.5 KB (25517 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:a64e232d16eef4c5d17920af0da61d9c403c3eb6a2ebdf18005c1c8f8e25c705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33968030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a12d896aa51c48bd6952b399a34073e8f4a25399c59108c4b31bb87d28bdb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
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
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7c5e817a944067a3cf1962ff180cad94ee4571b3e8ead8727259c76781b02e`  
		Last Modified: Tue, 01 Jul 2025 02:16:33 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f697b3de816c98d9b7a1c7b332eb9b69b3d5272a98566d2d5cfeaeefbbafb3`  
		Last Modified: Tue, 01 Jul 2025 02:16:33 GMT  
		Size: 2.5 MB (2502678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fac50950f7ef82623e0addba482a40cc292824f022ee35dbd8d2978b67ce94e`  
		Last Modified: Tue, 01 Jul 2025 02:16:33 GMT  
		Size: 2.3 MB (2251407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a5a825f627106e9978fca6ec83d4dd6961e01b3a3ee4e0e0aa2683f8e599ed`  
		Last Modified: Tue, 01 Jul 2025 02:16:33 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88ec267db6721a25fc14e609add201fd191e36606d7fcaeb6d9bbcab987b1a5`  
		Last Modified: Tue, 01 Jul 2025 02:16:33 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:bfe143a412236a03c2e419864b8e283625d20c65ba922473be505d77f2def7f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7963ae27e824f4298c861ad7b57f0d462e70ae03cec3cd6e9f5fd7b5e470eba2`

```dockerfile
```

-	Layers:
	-	`sha256:ec34214e08a33654cc41dad08f2894070b9ba52ffa25ff952496181772fa1fc1`  
		Last Modified: Tue, 01 Jul 2025 03:34:47 GMT  
		Size: 2.4 MB (2397127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e4159ab4e8dd090fcb07c728b366b31c79c430f7e1256d29e3163410cca7f14`  
		Last Modified: Tue, 01 Jul 2025 03:34:47 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:94a555ca272786824e117dd399adeace6af620bad74977cc29ddb6566ad255e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32779476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a302259d7565707a44d6d4ef36b623275a67e0eede00a48572184557f061e0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:fcacdf0767dbc0b08ad73fb46ff36dc2ec6b87367debc1e5018464dc1d3d7035`  
		Last Modified: Tue, 01 Jul 2025 01:15:02 GMT  
		Size: 28.5 MB (28516734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e746c61526650109c975e22ef1f0fd6a489da2a8274c2b717d31b7f8fb0b01`  
		Last Modified: Tue, 01 Jul 2025 03:23:11 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888449be5414b258ec058316426249a5261f5e560e7f4e7178416a30bfacd692`  
		Last Modified: Tue, 01 Jul 2025 03:23:17 GMT  
		Size: 1.9 MB (1944095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987e25db8d821b745e82a3a043cd707c27dad31b61725cfb70d10240c78a3223`  
		Last Modified: Tue, 01 Jul 2025 03:23:13 GMT  
		Size: 2.3 MB (2317135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83645cce79f5e98c50a2d797416c64f1ac56d3e166851a3c6f37db5f56232e7`  
		Last Modified: Tue, 01 Jul 2025 03:23:11 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3af65f28458685dbcea1b6c87ae7d9680122c2bc2ba8c5dfd2e20ae5e42bed7`  
		Last Modified: Tue, 01 Jul 2025 03:23:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:2d673ee311c79c830c3adfd8b77279669225090b6fa71ea1dd058b30496df77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48da34577e1c5c18a1b0af13c1d11f77faa4f6338f9d2465ee75f0240b168531`

```dockerfile
```

-	Layers:
	-	`sha256:b80163597d77bdf50f2e39e43cda89823c145019ec8bd9c33f6fd2162b8359e4`  
		Last Modified: Tue, 01 Jul 2025 06:34:47 GMT  
		Size: 25.2 KB (25216 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:d0a14a7794ad20f54fa6379130119368552bbd96e610201094d8afbc8f2e5d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37203469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8acb9e3c5fea408a5c0419d235d694a435e096abf6e13faca319ef0c572e008`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a863ab9441b0b8cc2b744ef5f39c29f0f05ed48ac8b68a2d5ac75c2312dca75c`  
		Last Modified: Tue, 01 Jul 2025 02:38:30 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1118ec54ed2429852c53122e14756d15d41e9368d00e9c6c2504e5e2dd526df`  
		Last Modified: Tue, 01 Jul 2025 02:38:30 GMT  
		Size: 2.7 MB (2710144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67927590d2e1939d7f51145cc076dfd9f387db5008be7f3d05421b2ee991245b`  
		Last Modified: Tue, 01 Jul 2025 02:38:30 GMT  
		Size: 2.4 MB (2418988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0214428f71307c5fca76e124602f31697c22efe58ad638f064e8e256671ee9c`  
		Last Modified: Tue, 01 Jul 2025 02:38:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2b32a175d879d4edaa68ef0d66c964178511721a5ed9963400cd619ca6af99`  
		Last Modified: Tue, 01 Jul 2025 02:38:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:7b4121f4871c93fc9ad3bd18a5e4112bade572bcf4f88ab9fdde02a0587a3445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6e3d91237aaf2a09683b016f0f4684dba1be3bf03e1b04575e1f915be0a61b`

```dockerfile
```

-	Layers:
	-	`sha256:7d9377fbb1fa0d501113906a1bf48b1bb1ce8d019cf292c2a5ef70a9e74dbc6d`  
		Last Modified: Tue, 01 Jul 2025 03:34:53 GMT  
		Size: 2.4 MB (2404456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f23626cb33252dcf7a955985f1cc58e867168828c6d54fb56febf620519f33`  
		Last Modified: Tue, 01 Jul 2025 03:34:53 GMT  
		Size: 25.4 KB (25394 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:7fc4ccb7bbfd5e448e450219e8613ba4f87903fcaaae67139627d27ae36409a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31309822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d870b0a32013dcf6c176224a1ef13f58885e4a5f88426cbd6ef318d60047e2cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 01 Apr 2025 23:49:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9b1e72f203f8e2e09f3010c996c0fe14f469085012c236ccb8838ff8603b5b`  
		Last Modified: Tue, 01 Jul 2025 02:29:53 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e323fc0d7148d9f4b752ba5e0210639a2f554134c9fb716a7491db0970253e`  
		Last Modified: Tue, 01 Jul 2025 02:29:54 GMT  
		Size: 2.2 MB (2156926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba661bb17bb441a1e52d0d32a6fa1949f7d4b136dcc63f12218b4b5fb8d4e6c`  
		Last Modified: Tue, 01 Jul 2025 02:29:54 GMT  
		Size: 2.3 MB (2263574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c3cea69ca9a7c76207eaf1baa1fa1166fd51cc1b8bc03a235dd2f0b7b436ef`  
		Last Modified: Tue, 01 Jul 2025 02:29:53 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3f21358b7724df003c9ecd5b18ce52e1761cb769af3fd5057ed390e19e549`  
		Last Modified: Tue, 01 Jul 2025 02:29:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:fd97905fa2d3f57013faf7bc1fa97873171d818e34689a8d4cef2bf8d0703499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ec0f733e3232db3ed9433c3ded7d0c2c43996a6cef019ce0d69b4680e448b7`

```dockerfile
```

-	Layers:
	-	`sha256:3155739622dfb39ca7c89e8f5d865148608401c7f7f9fe61acae35f7492e8331`  
		Last Modified: Tue, 01 Jul 2025 03:34:57 GMT  
		Size: 2.4 MB (2396806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d048e53689c3440adbfc7da50fd1d1bd6008c1b152ddb0c681b5c326ebfc3510`  
		Last Modified: Tue, 01 Jul 2025 03:34:58 GMT  
		Size: 25.3 KB (25320 bytes)  
		MIME: application/vnd.in-toto+json
