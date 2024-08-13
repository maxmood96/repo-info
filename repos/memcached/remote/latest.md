## `memcached:latest`

```console
$ docker pull memcached@sha256:040aeae958a32d668abfe37e07853dc62d493181db0606b9bee6dd5d6b71b641
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

### `memcached:latest` - linux; amd64

```console
$ docker pull memcached@sha256:022d49c9c0719720f94eedc3eeb9fdad274aa92c3b9f0353378b7af4a5030c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32871159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493a168c39be2478433b2a19b42d357d970b9e3b8f45d701d6ecb79bd34d45b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a619ace9775e35f0b996955eafd01e113c0f1040793964e2d13b672039d7c41`  
		Last Modified: Tue, 13 Aug 2024 01:22:37 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f83877d75663bc9e4dcc5445848da847dd9da27b66d6be0797098cb9e045809`  
		Last Modified: Tue, 13 Aug 2024 01:22:38 GMT  
		Size: 2.5 MB (2489426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ad79d272fc09adb89302b82fe44073563b098ca93887fb765811a09e16e299`  
		Last Modified: Tue, 13 Aug 2024 01:22:38 GMT  
		Size: 1.3 MB (1253989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcbdfc9a5a8a7f6102cb1da76ed1fff680760bca955de58ca1583e2f4d9ee3e`  
		Last Modified: Tue, 13 Aug 2024 01:22:37 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a18f32568d009f98d42f1c2dab0abd4a3fc3df1b8a676a4fc5c1fffabf84d7e`  
		Last Modified: Tue, 13 Aug 2024 01:22:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:433bd2ff8508ce9b42fce5f56ecf51c33d2d5c2d2b54f4fbb27b6bc2d1a01fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bec9ed046cb6a9499c21a4fce3be512dd4938073a7390fdbd24291ff100eb9a`

```dockerfile
```

-	Layers:
	-	`sha256:0ca0db4059f3fb6d91f779b380f3133a71fbeabe6dd1f92e431bf5def0707baf`  
		Last Modified: Tue, 13 Aug 2024 01:22:38 GMT  
		Size: 2.3 MB (2280679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abbaee022c08135c865790763c30bc91e63b8e5fb2bd891bf9d01d9cf3b1eb03`  
		Last Modified: Tue, 13 Aug 2024 01:22:37 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:13e3ebdd1012a6f48d309196208aa3aa9e6f515ecf89a79563df6fe5f607126e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30215737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75868b35a37ca53c05d87550e072e1b4ea99742e34b6d76441a9da245abb42d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:752589c0ca446e2e74ef0b8c412eabb01e2a8035cfec47b1d9630b9f704fbda7 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b695a3453560aacd42060f43ccf1cbd7d20412f50126ca6a469af38d3fe1e5b1`  
		Last Modified: Tue, 23 Jul 2024 00:01:19 GMT  
		Size: 26.9 MB (26887299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca2f192194ddde6c61f236b554013fac0290f8e6a66b698e1f4ffc626ec78d9`  
		Last Modified: Tue, 23 Jul 2024 08:00:25 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c545cf97223036b761763eebec2e73b0178270ae0d5737578efc8e998e6b8e2`  
		Last Modified: Tue, 23 Jul 2024 08:00:26 GMT  
		Size: 2.1 MB (2093187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b029fdec7f3eff1792b6d19990e428c1fe7c574d8ef1b0fe47c2edb597264328`  
		Last Modified: Tue, 23 Jul 2024 08:00:26 GMT  
		Size: 1.2 MB (1233738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c4f5e3eaa0b92756bbe621db21dc311afb19232bfcfa550184f6401a03250a`  
		Last Modified: Tue, 23 Jul 2024 08:00:26 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40057eef9dc899d2a6c18e778d6d0a9fbe9e13c7e9d2401bdd14d29060a9458f`  
		Last Modified: Tue, 23 Jul 2024 08:00:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:2eb710cd3c1b3e2bd338ac715837040ee1c61ca79b0968347b99fff4fc40da05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97dc722b90317466ecda7d716fa8ab4a1c4479d48cffa3ac68023e9fd32f302f`

```dockerfile
```

-	Layers:
	-	`sha256:7f7b2d8a7eef25468cac7402712cf09d15320676c9a4ce1c45a9bb6e7129cf7b`  
		Last Modified: Tue, 23 Jul 2024 08:00:26 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a91965cbf6e7e3930d2b1431fe39f2cefb15ca53d86eceb0fe60dde15a8c1c5`  
		Last Modified: Tue, 23 Jul 2024 08:00:25 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e48bbd3bdf087444d19af660bbb9c0bba24aebc378db00aec393fc0aa1d1a805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32760906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd3f929f5d06e33c27ae71f4c30580decedb5000e8959ca44ff03093c5ab33b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a49e80475d01789d42033cab1038768651e2d7960386eb5c03e802d0d944f0`  
		Last Modified: Tue, 23 Jul 2024 18:25:31 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff16aeae2e7120473528b1043ce5ffc020bcf62a41b1275f1aa6bdfebf810b`  
		Last Modified: Tue, 23 Jul 2024 18:25:32 GMT  
		Size: 2.4 MB (2351828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690dca6e49484fa87a45319f43d3887726b1c84aa8d4d926c457f502fa4f7fe0`  
		Last Modified: Tue, 23 Jul 2024 18:25:31 GMT  
		Size: 1.3 MB (1250994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c30434df2569a569d9ef29fe1b8e7f17aedccfe3ad167e88d7ddba796fce8a5`  
		Last Modified: Tue, 23 Jul 2024 18:25:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740a1bbd34f7209b35c8fd8743e5381894385d13112e7c119695e357e5f5f3bf`  
		Last Modified: Tue, 23 Jul 2024 18:25:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:0f27f9d0ac4fd8a2f1896d716e1074e4e6ac3244b70ac8cb6d02f0ffce4dc770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5080bfc0bb3660e96ca856d3237799166e0a0aa5d921b04f34f0ad2ef0489c0`

```dockerfile
```

-	Layers:
	-	`sha256:8d56a6dd82d1449dd6651fdaa96c092d2edf698882473d7c8ac4653c06004682`  
		Last Modified: Tue, 23 Jul 2024 18:25:32 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48607f906e73fc77eeccb9ccf2c48d3ab73169fbbc764c21337d968d778aa3dd`  
		Last Modified: Tue, 23 Jul 2024 18:25:31 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:aa1e352b6493ebdc9e2fbb27bda1a53118b3d4ef8851deae89f4479673bfac73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33895805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b53930da2ee4671087de1682cbba4811696e7924063538e0a218957d16708b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:6c928b979f82a9dc0b3801b97a516aaa3d17fe57cb9eecc077d202afda56d2fb in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:82c8eed510ac33a6df3a546a738b1f3806df7958ea977484d0f77eabe177108d`  
		Last Modified: Tue, 13 Aug 2024 00:42:35 GMT  
		Size: 30.1 MB (30144281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41abec48b83d1989e7848fbb893fe86c7c85d79af30696cebe85fb3796c8660b`  
		Last Modified: Tue, 13 Aug 2024 01:22:44 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db830cfec629394b55e2649839a99204eac03d46c0d46a76c57d63e93f812891`  
		Last Modified: Tue, 13 Aug 2024 01:22:44 GMT  
		Size: 2.5 MB (2495283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047e06d3087d639df07e2fa2dd125556487f81492794e51f0630c9eb72261ae4`  
		Last Modified: Tue, 13 Aug 2024 01:22:44 GMT  
		Size: 1.3 MB (1254729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44015ee55952a77f87cc344c2a30f903c60e1d188b320daff14ee7aa62868222`  
		Last Modified: Tue, 13 Aug 2024 01:22:44 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c561e964604ed8d1ca64582ef567c8fae0c5c64287f8a725408d30069e64ff5`  
		Last Modified: Tue, 13 Aug 2024 01:22:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:abea52e79ac9b9e0b805910fbc5d026387c53be79ab87f6c252c0275bfcaca11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d69d90c14eff67ba27d44f1442442fe2cc5fb194661374ff7bf127a1cb3ecb3`

```dockerfile
```

-	Layers:
	-	`sha256:4ab82220cbb5e277707fde577015d5063eddee1bc369a255e2a090d7a7aee30a`  
		Last Modified: Tue, 13 Aug 2024 01:22:44 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3762f3b65a58d41ce2a496e8af9277808b5093865fb00cf8ab58f169cdf2a41`  
		Last Modified: Tue, 13 Aug 2024 01:22:44 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:9d2c924ac8f6453909191fb725bdf2c99840ee54f0d2244de5c8c9367fba8a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32317069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ae118093e348687522ff54ae265f2717767a76c181b4938974c17e6db9e1ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:6b0de87e15c6880fed3a8430d23a511322519e32c50677c24f4597141e3a85ff in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f8de7af9de8596141237ef7c589f08f773ca8ce07671b2bd7e192055d5165f74`  
		Last Modified: Tue, 23 Jul 2024 00:49:06 GMT  
		Size: 29.1 MB (29124926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b1bf3fe66c8dfd264b314321094f57909cc8d66d1eb2e41c9f7557a7cffc7c`  
		Last Modified: Wed, 24 Jul 2024 03:53:25 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20de6dbc4faf9039ea9ab3b81b341fe6e97cbd59e6ae195afb73542d17e71c8d`  
		Last Modified: Wed, 24 Jul 2024 03:53:26 GMT  
		Size: 1.9 MB (1940979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee198b328ab1a37dc6f27cc1e4ce27a0cdd46404b1b90e52b35a0a8a9fdfa7e5`  
		Last Modified: Wed, 24 Jul 2024 03:53:26 GMT  
		Size: 1.2 MB (1249650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c08fab510a10791cf7c7029f1d95a93f6e5dcfaf377b753ffcafff01940789c`  
		Last Modified: Wed, 24 Jul 2024 03:53:25 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1069c5fe23d443f1e890273a042c831d1d2cb0748093eaeb21275e209c9e0c0`  
		Last Modified: Wed, 24 Jul 2024 03:53:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:ff6cba5f744339977de9773167690fef8de7afda3257c67fac44bf626e77ed47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0963145cb8edeaef3a54baadf843723666353505fb1f6b27e9b58861286eba97`

```dockerfile
```

-	Layers:
	-	`sha256:84dcafb21a7941ca058649a0a63c58cf93e3df499561fbb3056d5fcb60d1624d`  
		Last Modified: Wed, 24 Jul 2024 03:53:25 GMT  
		Size: 20.9 KB (20910 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:d1d938ae46108633b1036e62cf66b7d8cf78a9d3c1b361e5db2fc8e6038eb716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37146665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30992250e98b75cc3414c5b7b81eb83c78a1c6bb0a7afa8c606bd868c5482979`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83d8098c0b5a31ca0ade8ba48b76e12e6ad3bccf59a71c686958253a9197e70`  
		Last Modified: Tue, 23 Jul 2024 17:35:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbee9eb6d1f6bcbb7d51a49cbad536698fb5bd43d21cb4fd3bf9a285f0d0cd36`  
		Last Modified: Tue, 23 Jul 2024 17:35:19 GMT  
		Size: 2.7 MB (2703072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8d93e2a06dd2beb9ae982c1449ca3f89d4d085b5ed7f66f97e9985372c0a7a`  
		Last Modified: Tue, 23 Jul 2024 17:35:19 GMT  
		Size: 1.3 MB (1319804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5147b0f984733675b267cc3755b148737d8af0ccc9305f19e1fd7200c04ff5`  
		Last Modified: Tue, 23 Jul 2024 17:35:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b76347227b0893eaa8d950a74524c6210502f6d312007bec7d61c244a6d9`  
		Last Modified: Tue, 23 Jul 2024 17:35:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:081e4a41fe60484a891b397e0fee6ad1e71d135899e113db1d5a06697b24e357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e286bb7d8242742f93b95c935fa23be65ebda2bf4d0ed0a63939214179297e84`

```dockerfile
```

-	Layers:
	-	`sha256:792855414893a54c6e8920af4e70c9eda58b937122b94aae32ebe4fb7b18a65b`  
		Last Modified: Tue, 23 Jul 2024 17:35:19 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8423a7554c982300bd86cce83d7f7781c41fb4ff77d38bf73989a15675efcb0`  
		Last Modified: Tue, 23 Jul 2024 17:35:18 GMT  
		Size: 21.1 KB (21096 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:ea616d05cc021027ea3f91b8b3db46fc81acb76709fb72e9b5d9b21e061ae9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30878881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:315275a42ecdd591a771d80b837aa32a1d407ce9158701d09b7ecb15070c97a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:2e68e80c30908adf6b4b6a8ea2cb0711c5b296a8ba63e2cff3b70422a4daaf97 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:218a263fc97fdfaefe7df9b0e23e00c5a0b71a094fd212f91621d5683c6e3514`  
		Last Modified: Tue, 13 Aug 2024 00:47:29 GMT  
		Size: 27.5 MB (27490097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3211338b9e1c30a9b470c1c47d011b66dd8a169a3cd035f8d6cb36192137c98`  
		Last Modified: Tue, 13 Aug 2024 05:29:10 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4536ba319bb35ac2f867702a8ae10eb1a17af55f16a6f95b98918839d2bbaf0`  
		Last Modified: Tue, 13 Aug 2024 05:29:10 GMT  
		Size: 2.2 MB (2153930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c7bb1eff67624e71ca40673c190ab1ff10fcf2aad460a733ed5d86982e6a35`  
		Last Modified: Tue, 13 Aug 2024 05:29:10 GMT  
		Size: 1.2 MB (1233343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3aeb0e25b50b461a538a133b56c5e5c8910f5e665eb0d16cedb4f1a78f9c5e4`  
		Last Modified: Tue, 13 Aug 2024 05:29:10 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5996abfa28dcc99c13c4672cd82095a53151184b637dac367292c3c80c28f06`  
		Last Modified: Tue, 13 Aug 2024 05:29:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f97415dad9f4ea6bfaa6ee81d9f20123afd0532ed2c8293d03cff153a4ccb502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b3f5282f852dd147efe2e8e874d1bd8f2aed26e72c2de5e9d4efc28e0ee604`

```dockerfile
```

-	Layers:
	-	`sha256:da35a5a2d3ed73619869cea8d68468e776cb28a68ec7baa55c79d1b966159b04`  
		Last Modified: Tue, 13 Aug 2024 05:29:10 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:434dc70b84a8317fc067e8ca9b39c622a24f410d089e81c62641adc0aa12ff46`  
		Last Modified: Tue, 13 Aug 2024 05:29:10 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json
