## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:31f8eb2c5616b569b9c3296bc8f98a329ae7e7762676f7c519e30a955f3e4d07
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
$ docker pull memcached@sha256:7a15a57554a88bd1700568812dc4197ab730d74422775ba0fd0db4c6786bfcd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33000870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abffb3a574215f5758d6774324b48641164eb059904eac1054bff01ec2ddd53c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Thu, 27 Mar 2025 23:22:19 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 27 Mar 2025 23:22:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 27 Mar 2025 23:22:19 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 27 Mar 2025 23:22:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 23:22:19 GMT
USER memcache
# Thu, 27 Mar 2025 23:22:19 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 27 Mar 2025 23:22:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b404466f8b3a70e1f985894a40860e3cd4f9dd47309d9752720e01d05c5a7c28`  
		Last Modified: Fri, 28 Mar 2025 00:01:55 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9dc057d472462f705438792c503b637fbad121b9fb84cd9636c3c7944dcb71`  
		Last Modified: Fri, 28 Mar 2025 00:01:56 GMT  
		Size: 2.5 MB (2491788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcad790b498a70182c1ee4ab6bc9dfa46b893b2e33a4819caceca8e874f0aab`  
		Last Modified: Fri, 28 Mar 2025 00:01:55 GMT  
		Size: 2.3 MB (2302704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10309b816fb241043a80c55193f78e93a096dbce9b9200a7a64a6206e9628c53`  
		Last Modified: Fri, 28 Mar 2025 00:01:56 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6702d5308e710bf880cd4f48a51ad26521e8d44ca3b8c0e74d10855b0208a9`  
		Last Modified: Fri, 28 Mar 2025 00:01:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a705cb2ce2779e28ced48346177dc5411e12cc937b742150a7c1469b52afccf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1948a32879f97baeacd898d9135236d4f1f9e601a9e3df8dc89af0769226dc0`

```dockerfile
```

-	Layers:
	-	`sha256:d6b5a39303dfe33c094093eb498ec96461c929400e6f96b16c8b320228bebe1b`  
		Last Modified: Fri, 28 Mar 2025 00:01:55 GMT  
		Size: 2.3 MB (2289333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cbcdbd903f7ea7a62a3244c75454641441ee28706c05d35d82823c9e0f72775`  
		Last Modified: Fri, 28 Mar 2025 00:01:55 GMT  
		Size: 22.9 KB (22874 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:052c1108cdc0fed4eb232e603861c98f68963cbb77aa249d0b5de44a3bac1389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29079648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39494a8babc1367feeb79d44c8afd733428aceae503a3007ee47b8828e43048b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 20 Mar 2025 00:54:12 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 20 Mar 2025 00:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 20 Mar 2025 00:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 00:54:12 GMT
USER memcache
# Thu, 20 Mar 2025 00:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 20 Mar 2025 00:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:87c352465466fcf04c9686fee29c2541af5fc39172801545bb24d9faa8cdeabb`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 25.7 MB (25735853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582aa80e513a22785cc5ca8afc34dcaecd6b2676ee7861e0b459dfcae9754ad5`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17ec5309de3924838ccbf6a9a035ad50b95939b0e23b35e7fc4790fdf9b7c1`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 2.1 MB (2096160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c4e1b7a6a3ef0d51164118aacc2da103f47ba71395e6e17c332b17a38bab2f`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 1.2 MB (1246122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f1cf9feb5df466da7d811f19683239fb9588250bc4d342106c598344d243c6`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a717ad7feee98fd6d3c266f693d3c7330f2b11324c091228113dce25fd4edaff`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:66be60c91b515a69d8254e7f3ebe7e0912f539b534ec740acf5c4a896d2c9efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734bf2e0a27785f9e325b4d7c1725df82ac83a9cbf94844513e75f6c7f4ead44`

```dockerfile
```

-	Layers:
	-	`sha256:a891ef46da187ecd2bcb8613190d77a7e57cd6a6c93ac280d1140df625a67766`  
		Last Modified: Thu, 20 Mar 2025 17:59:09 GMT  
		Size: 2.3 MB (2292871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceab285d85e8fb43c253907f96b38efd60941056b3cbea822e3bf9d685672d73`  
		Last Modified: Thu, 20 Mar 2025 17:59:08 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:f989b2807d3d217fb2b72bba16774925f37b670df69ec695a59334d124f19dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32689604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba60fd8fe4c1452a0f969fca95cd2ec3e54c6b010f91af1ffe464fedb0b429a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 27 Mar 2025 23:22:19 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 27 Mar 2025 23:22:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 27 Mar 2025 23:22:19 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 27 Mar 2025 23:22:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 23:22:19 GMT
USER memcache
# Thu, 27 Mar 2025 23:22:19 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 27 Mar 2025 23:22:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebf84f2349518c66e30c518385e9db263b07127df1e1243f71112868417cd3d`  
		Last Modified: Thu, 20 Mar 2025 17:59:02 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1a4ec0e67eba4119ea3e9093e1fbec835abb85c1182c5c4b5cf62b1e983a3a`  
		Last Modified: Thu, 20 Mar 2025 17:59:03 GMT  
		Size: 2.4 MB (2355308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16469ca78ed6c39712e7afdba274d312eb5f2db769393b093b6d590a78539a56`  
		Last Modified: Fri, 28 Mar 2025 00:00:49 GMT  
		Size: 2.3 MB (2288746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6dd42acd541ee79a0def2949ee9a3c144d334b243df7491bd75140c4c8c0a7`  
		Last Modified: Fri, 28 Mar 2025 00:00:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b70a04dbabafafa6182fa8c67871ba1889d105c79d2c580c5a6e332352dc2c`  
		Last Modified: Fri, 28 Mar 2025 00:00:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:549c920e6a8804fb4046ce91ce13adbb70c38682057735809ea3bb8d6a4a1ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4deed5e744714f6a49c1f96c0524b445effd31e53648efcee9f7fdf22d7124`

```dockerfile
```

-	Layers:
	-	`sha256:33c13879fb2d6d2f09e7897418a35cea58f855965940650726a25b5e9e040c0d`  
		Last Modified: Fri, 28 Mar 2025 00:00:49 GMT  
		Size: 2.3 MB (2289648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0696dc07cafd0763cdd8d5dbdd302e2c7b83ca98c25acf3a7411600a645ca948`  
		Last Modified: Fri, 28 Mar 2025 00:00:49 GMT  
		Size: 23.1 KB (23071 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:195a42effd3e68412c7c923f4e17ac1c1ff1a0243abf5cf246b9c78764c37b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33943014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8242c16ac70d5326081b98813156e70e5f5b95a985ff03ae361d6b8cc06d42df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Thu, 27 Mar 2025 23:22:19 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 27 Mar 2025 23:22:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 27 Mar 2025 23:22:19 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 27 Mar 2025 23:22:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 23:22:19 GMT
USER memcache
# Thu, 27 Mar 2025 23:22:19 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 27 Mar 2025 23:22:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7c9255a65ed5f24dc5ab95f9cc0a8f6bb676bb640851d71c38bf7eadad1569`  
		Last Modified: Fri, 28 Mar 2025 00:02:26 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae82f6df9d1f725cba9e099322ef1b75320c746e2afa4a7b8b55a1a14fce91`  
		Last Modified: Fri, 28 Mar 2025 00:02:26 GMT  
		Size: 2.5 MB (2500754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de56f3bbbb7a379f62fc215bfe1d6bb29815443235a47b9873ca81ccad186bb`  
		Last Modified: Fri, 28 Mar 2025 00:02:26 GMT  
		Size: 2.3 MB (2251216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52e8e2d9948733e0ccedcf29835205346c4167a478c4aa401e85d5f540a5dd7`  
		Last Modified: Fri, 28 Mar 2025 00:02:26 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f2d648de71e50b5fe005f414d20dbd69abd453c39f26c551a618b3e2a8937f`  
		Last Modified: Fri, 28 Mar 2025 00:02:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3da8e76a946bfb75cf558bebffc8a9400906995ad9790d91aebb67016143bc92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9cd1f999bdab993e8389bc5ca518f411767f54f178f0bf776d084407cc0978e`

```dockerfile
```

-	Layers:
	-	`sha256:e05212e487c3668cfad9b4072bcb6664b2f12008fd193b8702f4040e5156930f`  
		Last Modified: Fri, 28 Mar 2025 00:02:26 GMT  
		Size: 2.3 MB (2286432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8106d720f4a2b267c46d2ee0b0d82c341009cbc49ba5e55b9f65542cc790c9b8`  
		Last Modified: Fri, 28 Mar 2025 00:02:26 GMT  
		Size: 22.8 KB (22816 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:56d9df94bd6f3be8554075083462d95f5ed206a22e26cd3bb432d0cd136aad48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32751154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac18b94557d0d94f434b54e9dd1111ea3eb51bd4b1939ae3703b01cc47988fff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Thu, 27 Mar 2025 23:22:19 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 27 Mar 2025 23:22:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 27 Mar 2025 23:22:19 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 27 Mar 2025 23:22:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 23:22:19 GMT
USER memcache
# Thu, 27 Mar 2025 23:22:19 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 27 Mar 2025 23:22:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18c44d6735d044d9bace3fdbe647c9b8187637683376f05d85dcb1185876721f`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 28.5 MB (28489456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1cab517934dece831db48577cfe017402465467401c3034d8bbb100cbf4831`  
		Last Modified: Tue, 18 Mar 2025 15:47:39 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57099e55c8442457b333cafcab5fe732b5644caf0416389e1cbb5a69aa0d2410`  
		Last Modified: Tue, 18 Mar 2025 15:47:39 GMT  
		Size: 1.9 MB (1943213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7675bb13fadc95e813b403bf189b3377efe8b3e5f14d0c6af4c280537870ad3a`  
		Last Modified: Fri, 28 Mar 2025 00:06:08 GMT  
		Size: 2.3 MB (2316974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babe52c076035e9371dbe7f6fe208e15771d05b6661fa383c4af5b43392749a`  
		Last Modified: Fri, 28 Mar 2025 00:06:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1cb9876cf09b424ddb35076a9116e6e5350d317f8ba46a198a6786a81708bb`  
		Last Modified: Fri, 28 Mar 2025 00:06:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:63a637578a40d2c2b34902a8b86697c04f5e68baadd9d5d91b444a84f3861e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 KB (22770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f32bbadf54d5481f1c8c3fc0d476dbbe1f5f741c52da8bd87f105babb79eca`

```dockerfile
```

-	Layers:
	-	`sha256:7c27d7bc8f3ddb49fb7a13adc07ff0bb010cec3f5cec26cd4e5e956b7d4cfd40`  
		Last Modified: Fri, 28 Mar 2025 00:06:08 GMT  
		Size: 22.8 KB (22770 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:7a7bb97c6c61dd3b4c61f8065dab499bbdfe7cfbe4cb956effa9edcb2e66af3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37176878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc98e5d5a70cd46d1686601994b63dc20ca2175f52c40dba598b762926e2a37c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_VERSION=1.6.38
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Tue, 25 Mar 2025 17:04:29 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Tue, 25 Mar 2025 17:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 25 Mar 2025 17:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:29 GMT
USER memcache
# Tue, 25 Mar 2025 17:04:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 25 Mar 2025 17:04:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd26e791f0c754bd4ee036131e4d6d631f455847022b8c48338e3e6189281e1`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ee71d1a4307eb0c556a4b387c35ea82ab8da5201c2647613b13e0a4afd370`  
		Last Modified: Thu, 20 Mar 2025 17:59:31 GMT  
		Size: 2.7 MB (2708621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253d36c80692194d710c838a9dcf641b5f4e5b708caf7a0167a65231d784da21`  
		Last Modified: Thu, 27 Mar 2025 20:52:14 GMT  
		Size: 2.4 MB (2418931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815dd2a928bdc05f75187e8f6ea5d86523616fee3840ca9163dbf320a5a6ccc7`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121efc6039ff41bfa98a9b47bcf4885d5e03c9456814d0361df3e771d123d137`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:d58f5f6a5ac867f60ce3aadad1e9917e3c03c7abb83b35be66d9f4cdcd7be38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8bcaaed8fc07c31e2e028ca1bc38f788ad0afe190b58e4ba7e054fcb4f4340`

```dockerfile
```

-	Layers:
	-	`sha256:27246f4bfd4ab676df1caa36848b296c12c320d9fc5d0b12540a193755ca7353`  
		Last Modified: Thu, 27 Mar 2025 20:52:14 GMT  
		Size: 2.3 MB (2293705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd9de6d66fe54e520712184227e13e9b50f4e82e578f5812610dd60205ae9f61`  
		Last Modified: Thu, 27 Mar 2025 20:52:13 GMT  
		Size: 22.7 KB (22747 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:f41d15ff160efd1053b74b9971c10bd87782c4578befa53cbe118a7d2ea07376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31282499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5005cee4735529479ec15fd4d43f0404f1bfac64026a4cfe984aa5f7ba2b4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Thu, 27 Mar 2025 23:22:19 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
ENV MEMCACHED_VERSION=1.6.38
# Thu, 27 Mar 2025 23:22:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.38.tar.gz
# Thu, 27 Mar 2025 23:22:19 GMT
ENV MEMCACHED_SHA1=2d132faaf4d4ffa4c1b5f55b2f09056a0e9181dd
# Thu, 27 Mar 2025 23:22:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		wget -O memcached-time-overflow.patch 'https://github.com/tianon/memcached/commit/8d4e02984661a3a26decc5a45d62a9eeaaf72986.patch?full_index=1'; 	echo '59f068d1fe4819ec65ec8c7adc8c5ecf8a7753ba5c6e5a17e5ba42c9946074a2 *memcached-time-overflow.patch' | sha256sum -c -; 	patch --input="$PWD/memcached-time-overflow.patch" --strip=1 --directory=/usr/src/memcached; 	rm memcached-time-overflow.patch; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 27 Mar 2025 23:22:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 23:22:19 GMT
USER memcache
# Thu, 27 Mar 2025 23:22:19 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 27 Mar 2025 23:22:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754021598cc0717cc674e4d6ddfe859cb62e41b396557fba44e12a1292b6c136`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbd154400277d46347ccf75665608efac006526f46514bfb15818f8ec020c50`  
		Last Modified: Thu, 20 Mar 2025 18:02:57 GMT  
		Size: 2.2 MB (2156405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb005a8497615674f355c670c5c2e38b8876c5be8b9a63dacec75d64db08b919`  
		Last Modified: Fri, 28 Mar 2025 00:01:39 GMT  
		Size: 2.3 MB (2263519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde8dedd56dd60d6ad43eee4018404ce8ee7396e705d94494c38769bc768bff3`  
		Last Modified: Fri, 28 Mar 2025 00:01:39 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2520b2248d58e9e246f05061d2cfe71c86443428bfea74cee7917c75902f2808`  
		Last Modified: Fri, 28 Mar 2025 00:01:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:75db427d96d5d0008b2cd593e33afbe0f0ae59c303994e82daacaedfa8e19ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e709f467e74a3902ebfb649bbb9a69105359bc279025c6c8a65d4f3cbdf38cf`

```dockerfile
```

-	Layers:
	-	`sha256:e79103493b9305fc449d2ade472d2c4963e4ec82838527947d0ea90db8ad93d4`  
		Last Modified: Fri, 28 Mar 2025 00:01:39 GMT  
		Size: 2.3 MB (2289047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:249e5d2876ee0cbc0d3ee245004e35a31bb621f07a87d1a6eff64f8db73b7110`  
		Last Modified: Fri, 28 Mar 2025 00:01:39 GMT  
		Size: 22.9 KB (22873 bytes)  
		MIME: application/vnd.in-toto+json
