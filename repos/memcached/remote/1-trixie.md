## `memcached:1-trixie`

```console
$ docker pull memcached@sha256:d8342fb8304c331cf074def075052dc891b0f38e7c4b5fa0b3760fe0439ad447
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
$ docker pull memcached@sha256:518f136cafc43439a777c20224d30b6fadc3433e3de9573f514dca10dd7e0082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32198630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec7b3eba028951d3aeee1ef26a365c913edaf06de6c008653f175c0ff0078ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:21:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:24:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:24:27 GMT
USER memcache
# Wed, 22 Apr 2026 01:24:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:24:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53e27a8dc2608bcd39496d6e1a0a021aa8933953409444f778d810ec220ab89`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d02c07f7ffb4ea4d70b3af1ed59da72e778c143718ba2a7bcb8cd6d12afd95b`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 136.7 KB (136658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b1a619145ef14a0e4599b98a19dbdc4fc96cfdf359ecf816454cd80ccf2dd2`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 2.3 MB (2280287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7716efee154a639ac02ada0d1638837bb72c3fc33ecac40f78ffb91daf9dfc5`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712f24abcdc2a432d57253a569a16eddd36ff1f8a4ace323467cdb642eae2850`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f32546667bf4926fd4e7c91aa55a833e8636777f2aa68437cb2bc7a5330e2307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3700c2c8b8182ac20db287282cdafbde42f55966784e109b48a9e5c2ba4d7492`

```dockerfile
```

-	Layers:
	-	`sha256:a3fe3f55746c35c0a798536b5abfc78349217684ca67ba43649a1c86d2a6ebe3`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0b151a6f180676864b1e8721dddbaf0c105e743520356d58f7df86572a295fa`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:df004aea9a02d7d4ee3ddc5465873404f20e8fa25c15e06d7b89d01d6cc1e356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea196d440f1b33851c03e3b418146249e09eb85317650c01e40dee92aa1966f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:36:58 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:37:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:40:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:40:22 GMT
USER memcache
# Tue, 07 Apr 2026 01:40:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:40:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28da11ded538198c9b718c34fa43b8c4def75a2f31b50ed3a8bda92c1030d2f5`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cec49185fb79e2c1fd6b70122aa01ed8d60551bf8210a8c1266bc57db7262b`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 144.2 KB (144201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005ba68552dfbe267043ef794ab62753f9b67961868dc0a9948a3d153a6ab565`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 2.2 MB (2211430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6514869f5fe8bb29cf6cd1481ed37590bf107b175195e617525696fe78550b`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff4d287d37148bcd3c24209d83e46e78903ea757dce43fd6afc57731e84f401`  
		Last Modified: Tue, 07 Apr 2026 01:40:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f240f6fbe003c002d394d498174c33dcc7af139322e3c52e5e090e7b49465c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483b0a17344b9495480290bd9db97e169606d4a2ba8364d8018cb7464afc40a3`

```dockerfile
```

-	Layers:
	-	`sha256:2be307cba0a326ce27f955114acf18cc984e34bd185e2aad06e8d42126d6e019`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1477528adcd0b2dbf9ee526a5e432557bcad4fedf5230183e7ba89f4132d2f36`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:4d262b60fea5a97e91a6c1827ab7209a344c47616388ada79b27e4e69eea9d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28516774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f2f7426f06caeeb218b724a947fa35544b0749bacf781227878e40cb98d08f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:18:06 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:18:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:21:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:21:19 GMT
USER memcache
# Wed, 22 Apr 2026 01:21:19 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:21:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0867e20c7ab47539b3f27abc4c7f4bf41d367127d9ffbd30a531ab387a69e2e`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34eedf23d5ae4af59fe6ecfd854e48545ede507ce44d930cea5c11b652b31f4`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 135.4 KB (135382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fff54fd1447de9c8b377640a2720588785769320b1a65d59a1da8e9690e6f9`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 2.2 MB (2165043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac214a1bada6a999cda6b6b021b8ef5ba954108062e3ee4df0161a500fc566f`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0431aacefa9d6f210c7c4778e75df5a21c196127779acc2da1bd7b32088f47dc`  
		Last Modified: Wed, 22 Apr 2026 01:21:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e4f840cb65bd892b2aafc305cb008de10d4d41475876ef9c9bbf51831f9cd7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987452d71cfba90bac820fca09f2954a061813125a8832038df5c062224577c5`

```dockerfile
```

-	Layers:
	-	`sha256:f5793a9489c1e1010726124554d7404a19b2675ce8596a38169b160edc81d045`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3c23077c5adc1a06a0e1f66d0ec1e57032a5b35685c53064098e236a62c5a1`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:52e2a52a542b0fff64533e7271ce3af9825a80a1126998cf6070b0ec4c0030b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32560736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3fcfefa704f0162e85ab03d515502e07a6ff91ec994dc4b6c956cc2ce80990`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:22:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:22:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:25:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:25:10 GMT
USER memcache
# Wed, 22 Apr 2026 01:25:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:25:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebea5231ebe63bff9044a4ee7713dac1b62fc15d85ee920f04eae4010a67b668`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5921030f644563277c2af1be27b21dfded0e01763210710efac613f07dc74c`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 153.5 KB (153515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1ef7f1deafd8e81fec98af35ef4fe12c2436c1eddb6bb87377b83f524f7d6f`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 2.3 MB (2262106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4f58ffc6f10cea1171fbb552aff0b93a04aba0ca6815cd9ad66ab3a49f8419`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace7ea462603345a875235135df0b8dd036890eacdb25150c1a8089604e3ca1f`  
		Last Modified: Wed, 22 Apr 2026 01:25:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:63aba0d160ad2159dd41a074d79446fc4ba2e745c7e5a10a41dbd1d5c2abc86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67f2365f86c60d496eb140fde16a0d6fbf89ae6a83d200c6a3971e32eca706b`

```dockerfile
```

-	Layers:
	-	`sha256:e87d247df404b9fe7e19667c95311e8109ea54acdcca2f52ceba73b7099d144e`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5290960be9e7480bf28bf59599ba02b7792ea80b3309570c3b3a24465ad7d58`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; 386

```console
$ docker pull memcached@sha256:14a8e0dca582269247d9148e01b5245b21dec2272071ca4f0de57bfe5da798ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20735a6c9bab36926f3fdc6fced1b8175cfe3f105a1bab23554f8456daea2896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:16:16 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:16:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:19:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:19:11 GMT
USER memcache
# Tue, 07 Apr 2026 01:19:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:19:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2980a28d02ccf82ab767a9e89afc9e4c15e85753a882a8a2263a2c0691a1004c`  
		Last Modified: Tue, 07 Apr 2026 01:19:17 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28192b8169c943bc464428731249fa5ca713d3be14de53eda8e012b20cabeb2c`  
		Last Modified: Tue, 07 Apr 2026 01:19:17 GMT  
		Size: 147.6 KB (147564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29865350ef2f7a2af74486f1fb3649b504a46931ac3e09e8a07592896b665b2`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 2.2 MB (2224764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d14265a50518850c61aebad318e069eef28a5e9b25658ec7de3279062fdfa0`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ce4f1d852aaa9c090f21a5e62d9c34e913461645b4111373022564ec41227d`  
		Last Modified: Tue, 07 Apr 2026 01:19:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0d86c338928dbeda1a6e986a64858fb0aed68a0f6c21e11882ec5ed8447078c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075a856de16e6ed042abc19a38a81d43d11ecd7a857943cc72e8b6ddd7313cdc`

```dockerfile
```

-	Layers:
	-	`sha256:e5945497f00077342a9e73ad0d2cbc87810b1953e63c42228d117969dbfec8ee`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46aed5ae982da715bb47a610f0f68cbf4b5326ce9401e5b9d9270b4aaeee19a1`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:92ac8b2eb8a499448552281cc533c85175af918bb0596c8dc74fd5b36a75bd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36159274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b82cf6a623a63a6ae0c8138a0541bee731e8bd82763d58be64d6699c425fe2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:35:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:35:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:38:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:38:52 GMT
USER memcache
# Tue, 07 Apr 2026 01:38:52 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:38:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eee776338abb1e966582aa93d7c23fd9fcd920abfbbdd3cea4bce8cf338f2e`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19eab5a207ad27e6d36357fcd01d34c3642fe0ed80f2f88a793cca9f476f30f7`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 170.4 KB (170414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625df055c4a6c1ff4e05c28e38811218be01d19aa2acc0795fc57b5de83d1be`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 2.4 MB (2394331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd4414756055219a9ca9c5147693091d8b0eb78130291d723e0cb2c9ce300a9`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635c499788fcf6fe44b99aac274f62a1c7a5da6cc7b5aa86372cb6073bb209b`  
		Last Modified: Tue, 07 Apr 2026 01:39:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:2c06d5accf94e67fd3485443b1c72edccb0acad4470fe42460bc84e82ae9e65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd4dbec1613b0c5fc1bbb19ba085247f554ca63690b28c52441c0b058dde46e`

```dockerfile
```

-	Layers:
	-	`sha256:c3f3c4328760b53a1cc92c96577452cafa2c7320c7ed12f724fec785c444f5ed`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc399d77df625da1dc8870003a0130dbe6e49e04edbd00017af3b4b6189acc2`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:343fd1c6e9e7f911bda94d07d87041db133ac3b59520418cf1583edfdc3ce77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30618876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8181bc4bb9dd1d641b682d8c26ed16fc76cbe854cee7b23e7f6ba281fb8047`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:59:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 05:00:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 05:13:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 05:13:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 05:13:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 05:13:38 GMT
USER memcache
# Tue, 07 Apr 2026 05:13:38 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 05:13:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172bc18e8051f399e255dee35e79f9e5fa9aa64562d2a8516dd4182f4d4520f2`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3677dcf4246be900eca90abef0e04b5b1e429066cc6b3a57604bd40e0c452b`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 133.1 KB (133140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03668775341afe9414f4c7e2652b23d3086383a5816cb62b8fb69364eff41155`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 2.2 MB (2208446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf395524f6f820cc7011bc1a2fcc5eba29e77275e6e044e4354d2614eea65f5`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f8103185e19fe4e971346e1109fa338f4d760dbb9e45dff1e3f928b8072dca`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b63ba37aad81705484c23176eb4f65464146117c69f7e8ff18a7768f27ace4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a87be3b1386b7e3afd6748a7748bebffdafd2e21f6de7ad9f393c6719938cbc`

```dockerfile
```

-	Layers:
	-	`sha256:e7592dbf997c4d12b7436af51984acabb26f49a58b3ee14c6bc50f79a06a1845`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f494bfe8ab328d634b3363d6b47b1bcc8e76f8982a3ffbb690421ebbcf84be6f`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:e0fadaa0ad7c323c4f8ead5d8e1ebb9566adc59b25cbc280f40bef816f9d62eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32280559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d7f2d629511f566dd7c4b3a944adb9989b05bb41dbd3e3881734bc1c1079c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:19:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:19:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:22:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:22:27 GMT
USER memcache
# Wed, 22 Apr 2026 01:22:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:22:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b460058bd06ca18e629070cadcc158edef16e034340796f661d4fab362ee94`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5386c57fa90d49931296cf79f5e8d2ae18d07b9bcffe5eee8354033fee4b673`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 140.5 KB (140521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd8308c0fc0224d29acef5aadae977dfea2e1ba7c9be0e207ee89c84a4f6417`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 2.3 MB (2298228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda405f0b2226447c88ba0d395ee00616ec775cecba66d9a980d4aac7b44fb49`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcaa079ef0e24aab0065df6b15e28d19a0807e2c9cdc639bbc63923135e6daa`  
		Last Modified: Wed, 22 Apr 2026 01:22:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7d2e45f2ecd9448a99f98a077da16fb59c37827c2acbac9e99dea8f79d753165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54358ef5a62ded9fafc9e908e79d81e5d01102cd4f2082017f54d92232acb7c4`

```dockerfile
```

-	Layers:
	-	`sha256:eb9c1105cc4bf8d4cf2089f7a2a43afe0a113388e7f5a4af9db1f44f9f0fbe11`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af1c4a20085e6a6f3d2b2fcb2ce9c10456d057c6905b84fe6ad6d99ba351a872`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json
