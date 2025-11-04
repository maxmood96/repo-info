## `memcached:trixie`

```console
$ docker pull memcached@sha256:050de63e6c082df85f93ffed9c388004b3c6257a06f1904e8628a6f87658eb99
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

### `memcached:trixie` - linux; amd64

```console
$ docker pull memcached@sha256:04cfb7a52848a5ddab7b57674b37c9b7b392d93ec11f0c9a4c300a9bbd1c19a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32209888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b3dcfe086b67312e8b165a92d8e71b517bf64b356c0c804270d2330e2577c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 04:05:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 04:08:37 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 04:08:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 04:08:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:08:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 04:08:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:08:38 GMT
USER memcache
# Tue, 04 Nov 2025 04:08:38 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 04:08:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dd2497c5fb854f1d1cb6790613048eae391c70dd7fe1d2c54ea024889782ad`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5e80885bbbbd2ccaf87a97c9f6da9eb3a9b7395ce5e2b73a110224cfbcfb1e`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 136.6 KB (136597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be7e82464812bb6ab2d37c74a6636ec8d73ec4154a192a75342dfa2f64cc8da`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 2.3 MB (2293674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18ba826b4b67fa295ff82d2b102a5f2db243fabcb7cc2acac6cc3c33a1cbf4a`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654bd5f6e9c2c18716bbdc27ac8f5eab96044427da57f1cb8ee268d2cd3b5f03`  
		Last Modified: Tue, 04 Nov 2025 04:08:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b78568d9b4a4cd24bae6187909a2a4a808abc29638602ee6aac1885173203e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b08f68a528f6821adc34258cb89e510c9bf97f5596cf2e47ce7b30ba202cea`

```dockerfile
```

-	Layers:
	-	`sha256:549c9101b19d3697bed0386c9c6378a334bce6d392f694130d47f2033273b571`  
		Last Modified: Tue, 04 Nov 2025 10:34:35 GMT  
		Size: 2.0 MB (2008234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c87354a983796083082c9e84ccf372217e5a602e78aefdec01fc26eae125ce`  
		Last Modified: Tue, 04 Nov 2025 10:34:36 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:cfd8f3dc480855d184b335ea9b7c334731ce495de10ef2f2f17b4f82bedf1965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fa3d1c819bb913d28b672eedf487f5165ff2dc4e5968326e550efb418196ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:24:40 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 00:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 00:28:01 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 00:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 00:28:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:28:01 GMT
USER memcache
# Tue, 04 Nov 2025 00:28:01 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 00:28:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da1461ffd1574069e2ddea407a8d31a9f215a260352498c03bb19d38c7d7ca`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4066eb4ba0932fcecba129384e7059abaee0e303654cc15d444f8c6aa11e69bf`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 144.0 KB (144040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f429e8aa4399dcb073c93dceeb4c04af1a46da5d750c71a36dcff1a94ab840`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 2.2 MB (2227397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100f4b89d2a8997d39ef62d45e5590e944f3120ba301e303025c7ccaac6da369`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334cb0302a41a8c70f7874d7de08c32eb550581a5fc8b17c9b565b9cecdb8149`  
		Last Modified: Tue, 04 Nov 2025 00:28:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:281d772292417096430072e287dae06f36229ebd35a2c308d81eccc1862e99bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956875d70010cc91e002ae89b4a07ce9edfc12bc2a743b377162df7dd92e6f05`

```dockerfile
```

-	Layers:
	-	`sha256:c19709d33e93cfcba6b59a36ac6efba06597c00114be0ab5c2aaddf33ee8ba33`  
		Last Modified: Tue, 04 Nov 2025 07:34:24 GMT  
		Size: 2.0 MB (2011237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60d569262f9d2f585a47be2ccf35c498002df82c55fd19ebcbaea6f9cd101f9`  
		Last Modified: Tue, 04 Nov 2025 07:34:25 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb4a02a784ff9c44adb4a72aa161b935ed3bd148e49b37fc5e68a1f3aa30a87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28532441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70b324b1a195c841f52ba1facea8f75482e1bb049f38d17f8a8b69185f65166`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:06:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 02:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 02:09:59 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 02:09:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 02:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:09:59 GMT
USER memcache
# Tue, 04 Nov 2025 02:09:59 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 02:09:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f9bebc6d7be8fb19e90bd816cf5ea46e325d9d8d019345bd7e83bb27165e1c`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d87b4f74b7b681280e1de65d55c7fef9af3294203ca9753541c48a7dbd67ac`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 135.3 KB (135301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012aaeffd16b06fc90dbc9cf1682d2a8cb96482af9e0582ebc1dc6881617ba3d`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 2.2 MB (2182590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30071a0aa370d64f866b34ab3ab9ed0d6e2f30dee5e631bc9b787ff5a9f4fdc0`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18d6989abdf4813c6c982f04f7bc42405ebe217f82671824a3bd75a1f923f9c`  
		Last Modified: Tue, 04 Nov 2025 02:10:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:672ae9e81bd13a12a5ae6790d4619294b51a1cfd04a6af50c523797512fc75f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95641a91a03ab503b7750055d3fe6cf1474b1c75ce6288b8966a514375dddb1a`

```dockerfile
```

-	Layers:
	-	`sha256:f13ec9279ccf6461d334439358fdee3b542d225588c6a3857991636d57ce10ee`  
		Last Modified: Tue, 04 Nov 2025 10:34:42 GMT  
		Size: 2.0 MB (2009694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37374c73a31babc67e99ab9936b2166b55c09c55f1bc4cfff80e65a3c40d5425`  
		Last Modified: Tue, 04 Nov 2025 10:34:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:bc5ac38c2657d7c6d375374985e9293fb3744a75edbd96cb7a7524cc14c95d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32572446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f397ae776296a0fd6edeebc664c5cc9fbc3f08556289a5a1fe41c75626d379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:17:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:17:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:20:41 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:20:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:20:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:41 GMT
USER memcache
# Tue, 04 Nov 2025 01:20:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:20:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db64d9b58942143a8d96f7823245feb1d4bf27c04222e71dbe7cedfce33d7e7f`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e45c84ea5c10a0167bca67aede44a66fd08b708143ccb896170e30885ea50f1`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 153.4 KB (153400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317fc2721e7de3ecc81d907c076c0de0aa0c4a80a7810a77e53335eab94adedc`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 2.3 MB (2275238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a6f24d2569f3c38db7873c0a8f3942c5c7b876fa9eff4eaeca997bc6dc28df`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9e0c677fc63b66e178f9171abc553450378c9046b77cbcc52126068101766c`  
		Last Modified: Tue, 04 Nov 2025 01:20:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:8d2e6520d11120bd0b01076b34657bd1b1a785b38c6f7048bc58db91821f584f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97a00b54cc845295e717a2bf8ba5f7b91d5fb25acd85c6c399b94596dd67465`

```dockerfile
```

-	Layers:
	-	`sha256:7061efa09aee437d8b815835ea3f0afa471b9f76cb95323b8260dc846c1f49f1`  
		Last Modified: Tue, 04 Nov 2025 10:34:47 GMT  
		Size: 2.0 MB (2008550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0254e16c47bdde3eb7e8d57383df36625fad7398861b5aca562e447505806a8`  
		Last Modified: Tue, 04 Nov 2025 10:34:47 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; 386

```console
$ docker pull memcached@sha256:e950b4f76df4b7ad0e9dcc9f2357df6ae35314e232ad23b0ec4fb3c3beb2b84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33688177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9910abbdac4661a59a1d8fe6b43f96cd0abdde92371f8c995e7216d706f375bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:48 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:22:46 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:22:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:22:46 GMT
USER memcache
# Tue, 04 Nov 2025 01:22:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:22:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6840654bcf5429c7954c0483368ccd033e4222b3098ca64904c590f04dd07624`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66205a10db2dcede178afb15530db6f282ec7194f11ffe734d9496d8b30e35a2`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 147.4 KB (147440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b63b70a9c43a2f37c5f37f50e2aaf507c970f0133b7aaaea29fdb4e826c18b1`  
		Last Modified: Tue, 04 Nov 2025 01:23:00 GMT  
		Size: 2.2 MB (2244441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a3c1d29eba0037255cb4c7903d5de630770804520cfdb28ce05b112d526ed3`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8da84bbfbc97884490625408deb986e43d5843e48291516064a41ab6d5963e`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:51b41d632670fe8c786707c7977f9136c593c137bcde08516527421769778ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7473e22367c8e8c736bb1ce76169b1b4abf93fa0b057dec9103c4dccf90efc2`

```dockerfile
```

-	Layers:
	-	`sha256:f90631de8235b43d3b44250b8606b5783cd39dc12e9810fb5993f82a19dfe2ee`  
		Last Modified: Tue, 04 Nov 2025 10:34:51 GMT  
		Size: 2.0 MB (2005391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d51086244a15fe10ebfe78e299fc7a89dd09601c8753741004d27949898c16`  
		Last Modified: Tue, 04 Nov 2025 10:34:52 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:ead041ea0e5c06d481ac304f7b4076a3339d849fcdffa3d25603418dc2fe82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b0128aff763178ac8bb867e486c2450bacad45f79a5ff629194be435141070`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:52:27 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 01:52:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 01:55:40 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 01:55:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 01:55:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:55:41 GMT
USER memcache
# Tue, 04 Nov 2025 01:55:41 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 01:55:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126ce0c080daa81edc8784c59f60350b32083b3201304709775cf554155f80af`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4c9857fe1f3ded2ba6c29c2f9591c7f5b2bfc46517527fac13f4c2b539a9a4`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 170.2 KB (170244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e15beeee778428c51e89d0b8c3d6ca7931f0324e0a66f6b2bf85b101e9674a`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 2.4 MB (2417022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d427e3c140105cfdb1a22a00010621a5a0834ce00ba3ea1059f8a63d8b0f5ee5`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dfc7efa96996e95dcf030731f854bc07f2c7aa3349e75c4e74c04d924b3c62`  
		Last Modified: Tue, 04 Nov 2025 01:56:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:ad9b48a87b820bbf6c20cb57cd2247fa75ca6de00df26576f784a8f51703c571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1582395261fcee60bb7362c6cff0abd1d7325b4fde3cd609ac637f76aaa7ea5`

```dockerfile
```

-	Layers:
	-	`sha256:f5e9fbdfb8deeebb9142cd4facdedb0629028f8343a64b1e13d26ecb035f3c84`  
		Last Modified: Tue, 04 Nov 2025 10:34:55 GMT  
		Size: 2.0 MB (2011835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3dd30af34832aa3d277b4b6882a9786e4225d5a7387d5af5a66cadc59adc22d`  
		Last Modified: Tue, 04 Nov 2025 10:34:56 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:56542c7304b39c7980a644419d2ab6f603477cc9e1cb9c575d45b8c4220e0c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30630140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e279bc62f41c4006902271742290cdde9d77c2121c1b4db697d09d01c690860e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 03:30:39 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 03:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 03:44:44 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 03:44:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 03:44:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:44:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 03:44:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:44:45 GMT
USER memcache
# Tue, 04 Nov 2025 03:44:45 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 03:44:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b836efb62045adb472c559fe0a4cedfe183f60ae9e36defd9b46efc4886fff56`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db437579ba55d9291ad05cd904e857adb520e8189f0cc2fb207b475c10a95ee`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 133.0 KB (132994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ca1f664c3ee469c225e4241d90dabf5a36c9fd5282ec51011fe16b9fcd5882`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 2.2 MB (2219849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5b56363e737d5d4b276274dc82b3ae7d3772bb1d6cadc5fb0c117ad6d004e`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92139c3e4198e9ce61d77b8a86d621938a3390898a4ac22ba81eefd286a78cc7`  
		Last Modified: Tue, 04 Nov 2025 03:45:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:a72757dfcc56cb3edf581d72aa35ca18e099d18284ccfaabc697a74b2d7c2399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a19d13356829e752dd3f0c530a1f2ef0abfc0ca53d29d3d74e1840a1698892`

```dockerfile
```

-	Layers:
	-	`sha256:78add421d4e1ac7755ca522075904f0acd06a15e1c8b9ca1bb0047a7d3ebf187`  
		Last Modified: Tue, 04 Nov 2025 07:34:38 GMT  
		Size: 2.0 MB (2002198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f1fc3731e375af1e0712ec91b83487acb49e907a1168f593f251fe43cb51fb9`  
		Last Modified: Tue, 04 Nov 2025 07:34:39 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; s390x

```console
$ docker pull memcached@sha256:3de73b4ecf32984b0c6603b973257071c81c94af8351b35aa4343407c7315726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32293163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6900a4460f82b0703aed07dde3c1722bdb7919a582b6b1f22a9ca701cb510f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:58:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 04 Nov 2025 06:58:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 04 Nov 2025 07:02:23 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 04 Nov 2025 07:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 04 Nov 2025 07:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 07:02:23 GMT
USER memcache
# Tue, 04 Nov 2025 07:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 04 Nov 2025 07:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17527924bc8c8387e810ff986ddbe9998a0b5d55a4850b90b4cea0a897c94a09`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54fd3d90bab9e973d6a8c142df91794bdc213e5bafe8926a58809036e1ee1f5`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 140.4 KB (140429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc993f31fbd52e75a8dfc710d94d4130a8c228be35b7737c5950a5f93a1125a`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 2.3 MB (2313833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acaa055d548771aab19234adcaf5b3ed727ee85214c303e1035e3e464e0fbda0`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c2e1b3aad04d0544265917caef9c91d5ed4496376262541974a707026847f4`  
		Last Modified: Tue, 04 Nov 2025 07:02:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:414b070c237a13d5dee83e1db26eb0f953dd5af0753013a8bbd988611aa90e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5cc4920f789bfe656195ac67c3ddd1a00030591f92b5ac4dc2b0e9dcdd2a0b`

```dockerfile
```

-	Layers:
	-	`sha256:b242fd5db27262af27c5589b736a5ae9f234cb03765c59c73e64818c1cade0c8`  
		Last Modified: Tue, 04 Nov 2025 10:35:02 GMT  
		Size: 2.0 MB (2009671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15d059f16d47b54c3d82bdf997670c62a062815b64d7e7b486d8de0060691b4`  
		Last Modified: Tue, 04 Nov 2025 10:35:03 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json
