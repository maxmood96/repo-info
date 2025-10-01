## `memcached:trixie`

```console
$ docker pull memcached@sha256:157c563eef6954ac0bc583c36def96d8ed2d3b3c5b37214f27d210ac53942386
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
$ docker pull memcached@sha256:b995c17f51fbc95ab650436bf004e0e08aac1e231a0c4ced640ba25409a53ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32209591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ebce0923097e2ebc228b419829228444709a8f2168920008cde8f0aacd5f50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339cbfbe5560ff0c225f888ba7ae149a9ce0536968c1bcccc467ceea4e3b09a0`  
		Last Modified: Mon, 29 Sep 2025 23:53:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84637889c9320e34d3cc8375e48fdc43299460f2280a8b62690c6d78f6a1ccf0`  
		Last Modified: Mon, 29 Sep 2025 23:53:01 GMT  
		Size: 136.6 KB (136571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe788cc20223f97addb89c197bd5ea5d77c3bbe084b00e8dcb70731168abb3b`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 2.3 MB (2293745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e090b148236c9a2470abf0308fbdf9c8ed3c23b04efdfb18e68f20902a2e2f36`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fa1d160038c361af454d4a8eb44b68dcda89fc415ad571b6e9707fb59a0082`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:5cd8c391814b8c7fbf65b5d657526c37f0516c6e4fe7dc245bfc347550a31200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40690a93df6f911472221738e6595b6a746bd957d3bf1552c92ff83f17536644`

```dockerfile
```

-	Layers:
	-	`sha256:4b787171563846ab285584301f579a404cecd6f570a25225e02ff18939e29124`  
		Last Modified: Tue, 30 Sep 2025 00:34:34 GMT  
		Size: 2.0 MB (2008180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5a013035c58f0ea6bcc734d2c89618a0e98d1d8b3d3f07a169cd97b52bf4c0d`  
		Last Modified: Tue, 30 Sep 2025 00:34:35 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:742d5665f0f292e1278bafd0dff520b5f4edb101c587c29fb0ef273f9d7e124f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1024c223c5953b97de26e48cce8df89bee4493e37781f6826e6df56c590056`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d24bdf1148108d2d3fc42a07dae247e5242de03db9a71e04066262a853f139d`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e717ac34c0d292ae77e9118ac1581d40d881e518d32d9e64f01fddf818164b`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 144.0 KB (144036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a3b7d16c874ce52964b6ba216127f7fcf604d326cc965210eb58119d605d28`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 2.2 MB (2227345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7f38fc7bbd06b5c988a48649d103d93ab0d8011b6a4f5bd8ad38bbd4cac432`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5307470e3430d06e3f04b798774d1905a98a13f5ba3387596a0aa97e34b7eba`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:92764b7963e735b77f5e5b433bf1311bc919679a81273cf442178538cf7da2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512f0e0d6001116f7984270337608de656664abeb7602b6fc4add42303ba8ee6`

```dockerfile
```

-	Layers:
	-	`sha256:a8fc1cbacd56787b740b886369c6eaafa6151c97fade289ea774600c03a80e11`  
		Last Modified: Tue, 30 Sep 2025 00:34:39 GMT  
		Size: 2.0 MB (2011183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57884b3635fcf7e290933e3a1da7210a05c98ab3187a6e484a5cc8cedf845e98`  
		Last Modified: Tue, 30 Sep 2025 00:34:39 GMT  
		Size: 22.3 KB (22347 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:889cba709c7ad01fa2925b49389f4e73f9d759d8020c2a108aabd5a1b1f2ee95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28532153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56676dc32ecaa308b63acf0b41885c581e3700d44bc04a653a595327d4198c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c067599f6c6ba1a22613aa308e4d66e5249d6cc507b1229b6f4d482aecce8a6`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cf0eec4f32f0da160c5e99bd0b57756034bb7093c545143caf6e310210cb44`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 135.3 KB (135298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e59b4e18c59ebfcadada2142ce2be01e708dd3af20396b507979cf3a15f6f22`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 2.2 MB (2182588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24488f6b368fccedb9bb9614c2c525964ee0e3cc91e91d2b41f74b38a1c9a59`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413fbe42e3bd71205a88a777ab5027fc34a2ad8053f6593d6653d72ae17ba8ff`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:ca8765c9f99276788e2b51ecfaf135680c03e0c222b9753d99dc4218bcc94095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6914431db285aeda4c9e27af56a106671c3541420f5b3bce905bed9f17ac6f`

```dockerfile
```

-	Layers:
	-	`sha256:fb1138fbff85001f5063fc6944faf0e66d26d9a179651b7a6b0c05c7f33a9240`  
		Last Modified: Tue, 30 Sep 2025 00:34:43 GMT  
		Size: 2.0 MB (2009640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c15f19f4d680266479069e896e888cb3a6a008b2f385c644c4f0baa61370937`  
		Last Modified: Tue, 30 Sep 2025 00:34:44 GMT  
		Size: 22.3 KB (22345 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ef5cebc6723efc4307b7e2459b1b2c096013265dcfc93ee6e929dfb04399da59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32570960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b078c21daa3a3ef97cfc057882f396e936961312205c8e1a12712f179cf9f15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c850e44210e9493ef7540c5c65cd48360355c3e6e94094c44d15af0045dc8dea`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a741f1a1ae0d87da15466cd2dafd5acfb37dd72d94dda9656931ef24906d618`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 153.4 KB (153385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa09f33f1e4c185a911cfd4dcd7d1dbbba5b9909fbe9100480230f1436457116`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 2.3 MB (2275224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a30963a9969bd789a111826840c0e97edd5d71548b548a30932bee7448fcc`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffdbd101cdb57f8b290f16ae4fa6106fd6ea85695fed7d08e98fdd19332d85`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:573b95a8bb8dd5178978144dbd1446143419bbfc4edb099c6ebbe467c8e00b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a5e2b768012fff6837a6324e893b847c3948649e73a49b722b5d6b4b2d1f38`

```dockerfile
```

-	Layers:
	-	`sha256:8ab701ab9aad8acae756d96838becc2299738dcbdd81cb0071e6fbb5459b2f5b`  
		Last Modified: Tue, 30 Sep 2025 00:34:48 GMT  
		Size: 2.0 MB (2008496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71a37a40aa0845aeb88bc64f742dc25764c4824bedfe40f31b6f13e0bbd595b7`  
		Last Modified: Tue, 30 Sep 2025 00:34:48 GMT  
		Size: 22.4 KB (22393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; 386

```console
$ docker pull memcached@sha256:0d993065ea1ed42de5bd4fcda3bafa779f274987bcb4d302b8a927344105ce6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33687876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe2c39bed6edf857f276a7b8e77499f6c2110ebe12362143053acafdf31fba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcd1d82da4702bb3c598bb03b9d138dea8bd5e459160d5276b3fb8ebfb58923`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ceba58f3514163ba75fa31b3b659efbe123eee61ee1e13161b71c6976b9cca2`  
		Last Modified: Mon, 29 Sep 2025 23:58:17 GMT  
		Size: 147.4 KB (147429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0453c4dd0d673c524b37cefb6f3412d20dde32e36c7999a26420bfb8481b0add`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 2.2 MB (2244401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8916b29a59d03a745388da5e0a1aae97b201cd0e333de592e8a0fbe93da42b2f`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28a35d7ac2cedad97d815d581ffa42e79c00126410603b586fb754ff264b578`  
		Last Modified: Mon, 29 Sep 2025 23:58:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:a1cbda14df44fff2e8baad5f7b53a3c32f617c55d96176326e107932e625e1d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef21897bb3061b8deedad86c30704928e376dad42a0a0bd9bdd946ff1cd46e37`

```dockerfile
```

-	Layers:
	-	`sha256:1f6010c4e760c848d7546664960f84f5082bc718d59b4dee6be3dc6489f1b283`  
		Last Modified: Tue, 30 Sep 2025 00:34:53 GMT  
		Size: 2.0 MB (2005337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f0fb1a46b98e7a2df02e226e82cd6854123a501d2d649bd70f05dbba8c4ffb7`  
		Last Modified: Tue, 30 Sep 2025 00:34:54 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:5a071a15dfae20029d56a8845f8053a4f4447934a87e0db0678b6f4ddc2e924a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6957fdbfa2f978334c6c02013b0e9b928534ddf41009ccae3597ccaf389fd455`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cee3e1fdea897c6a6b3a982e1918145b5bcd716e5ae6ed66b5e7184e651e059`  
		Last Modified: Tue, 30 Sep 2025 07:50:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dea6ee42e2fcf50b7f0d213d52ea27f8eebdaf12c0aa80c5df4828c4566af25`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 170.3 KB (170259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629d93745cabb21520c860c7612f141299a2c0f2632cf40b7dcc88799307dcd7`  
		Last Modified: Tue, 30 Sep 2025 07:50:13 GMT  
		Size: 2.4 MB (2417019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbd1630af2c91474bfc04cf614cc4d0a7093510b706f978f20f426127e93305`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8293ad839e50f443a419fb4c0f6a6dbde6204ad3bf467cdff6e99385a7d1c3`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:987b950cf472a2d95cc860d4c3c9e95c51ab792c33f5ac61607b7e4f38d1d8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973c6753846fed972084489bd202cf7da6e77ddc33d584a90658a8949b5730ee`

```dockerfile
```

-	Layers:
	-	`sha256:821a5821beef4d6bdae90ea0d98277dd982af05804dd43f706310bc7263244c4`  
		Last Modified: Wed, 01 Oct 2025 21:34:36 GMT  
		Size: 2.0 MB (2011781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:222d48bb5ef6a86d72ecccaf90a1cd7cf49c644139aee33815b1e7d0fd87cfcb`  
		Last Modified: Wed, 01 Oct 2025 21:34:36 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:31bb76b9b98cd96febc6b1d5056f839ffab9aaaa12690d0a47353df1b2b49221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30629784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e010912f76722a300766eb6afe7e6b13e8f72682c8dec557d00826b2a7cba503`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c2f28b5ea15f2b021d2f93df684963b9d27de2301bfccbf53d01abc5bdaa97`  
		Last Modified: Tue, 30 Sep 2025 04:00:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179b31cc3aad1ab89917cf87cb268b6e8e4291ec4b8996317231c4ac0003ebf9`  
		Last Modified: Tue, 30 Sep 2025 04:00:18 GMT  
		Size: 133.0 KB (132970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5db35fb11036dcb8f2d55bbe271869356c9b4b2e08c0d0293a9b0c894f5dff`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 2.2 MB (2219797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc4c908359c51ce26778438a3886b2eb2d6987ee3a22862dbdbe2056a3cd95d`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7254f9df049c190c1c3ffa9794b395fb4e3ec7ab18b8dce7a58733c63a54dd`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:10dcedf955ee46896155ca87f9a292967d1ce021fbab41f3a0fc44045a885e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a06d87da790b7800c970ca38989414eeae6c950cf890286591dc59c6163cc5`

```dockerfile
```

-	Layers:
	-	`sha256:b8fb80942d713e49171d0a98b2306b7bbb0023e57f180295e56893f7ea7f458d`  
		Last Modified: Tue, 30 Sep 2025 06:34:34 GMT  
		Size: 2.0 MB (2002144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cbc67dcbbe8db9619b2b3e3b962ebb7d9640901e2048fa63620351cc03d940d`  
		Last Modified: Tue, 30 Sep 2025 06:34:34 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; s390x

```console
$ docker pull memcached@sha256:97d22f11a028c8313d60f2b0d408dda8b2d48228b9b75aa2837e5463a793b535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32292996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e07eed38bed1a525726cbdc7874a25878c07feafb0bd683fe1f6583de2f83e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51adc9bddc158c97c423c25020f779f6eaf1052b5377d27f3c426f6e1bfc021`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e96b9e4bc41b016b366753e5d7d24d6ec0ad57f58fd33f9950ec9221297a8a4`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 140.4 KB (140431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e41252907eabe8a9429031bb41587143d8a76355a4ec8726199ab91669e2ec3`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 2.3 MB (2313824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2a41347a9c48966679d812976b6782615489e8d5f3d097e121b6150546f1cb`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969f1ab4db0027abb6561b0f8c35ae90cdfd2564247531bffcfb8860284b4319`  
		Last Modified: Tue, 30 Sep 2025 06:33:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:3f77e30f08514ef437bcf703e92082745153815200f728ce23b57a22ebbe9f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af62fcf07f143e611b564b8cdb2e08d11e05d8a8917d137e71fa925d6c936e4`

```dockerfile
```

-	Layers:
	-	`sha256:2db70adf2290adc880f8aa191f9e3b299c9dd28f01e3277a5386f4830c1f1f16`  
		Last Modified: Wed, 01 Oct 2025 21:34:44 GMT  
		Size: 2.0 MB (2009617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c002c1b0040529dcbb20761ae0b22e83c70cbf1d616626a80eff7eeccc02b1e6`  
		Last Modified: Wed, 01 Oct 2025 21:34:45 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json
