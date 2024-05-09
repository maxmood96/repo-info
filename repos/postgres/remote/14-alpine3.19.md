## `postgres:14-alpine3.19`

```console
$ docker pull postgres@sha256:8bacc66a9fe31b099a4ed95c345627af701d0e2d411c45c5538d96b88f5e20b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:14-alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:ac4ca373551069f5cceb157bc4ba7fefc67069f3cf7dfb96fa3fbfece9888d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94186652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd1dccf8db78e3a4ecf5746a81a74e6dc1478bf57759091fe2ffed6c78d2f3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_MAJOR=14
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_VERSION=14.11
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_SHA256=a670bd7dce22dcad4297b261136b3b1d4a09a6f541719562aa14ca63bf2968a8
# Thu, 08 Feb 2024 19:28:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:28:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:28:15 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:28:15 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:28:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54d40fa3899a525bbb99c32ebce8c195e7b25c87abe156b8197f8e4ef6ad486`  
		Last Modified: Sat, 16 Mar 2024 00:00:35 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bba88902c495619a79e90cd759e1e0787fcb2b941ae5afdfef06b2cc04470d`  
		Last Modified: Sat, 16 Mar 2024 00:00:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895cde69c46d0fbbf1863c26dcdcabf2e83c648e6e1b46399cee57b8beed710d`  
		Last Modified: Sat, 16 Mar 2024 00:00:37 GMT  
		Size: 90.8 MB (90761441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f283b4aaa3dcaa969eba9c4a0ba028141757fd3497838a036e9e08fc4c78b562`  
		Last Modified: Sat, 16 Mar 2024 00:00:35 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dfb80fbe96078085c608cb6142ae44d178f7cd02561afeb2896f728b27ecd4`  
		Last Modified: Sat, 16 Mar 2024 00:00:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab9af40886f4c0dd7e8ee4879a511d7fc5e2973e6772b5a3f01e8fb72f0d6af`  
		Last Modified: Sat, 16 Mar 2024 00:00:36 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0008d7ccfed1d634a28499fb861242579846ca925e577ccbb650ec3da7a9b5c0`  
		Last Modified: Sat, 16 Mar 2024 00:00:36 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f53a735edbf0fa3c8cd156ff886800fe0a6e218f2c8a47f07fa7d1e2aacac75`  
		Last Modified: Sat, 16 Mar 2024 00:00:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:efa53e1526dcc463d314a69bcb3e880fe3a8aff1f3228494929605a8d7e3e053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.8 KB (994847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca6347b0f43f71f8af17193f6795239048b673080ab6e8f25b8eabad20c7567`

```dockerfile
```

-	Layers:
	-	`sha256:8097c257d44a8e9979985f41b5048faa8a51cbc9d73f950bc146cfa3dafcd0c0`  
		Last Modified: Sat, 16 Mar 2024 00:00:35 GMT  
		Size: 957.3 KB (957313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:462900712394a61ed578fc1a343a62698d66e9dde5f5645313eb0afe9519cac1`  
		Last Modified: Sat, 16 Mar 2024 00:00:35 GMT  
		Size: 37.5 KB (37534 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:51e6cd983ef3d57e93f42edfae175b9cec70c70834408ea88969de8395fbbfad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94717165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61719fced3c9a9d8d4f337f10324873e25e00a91b75b8225c35cc0bf66e37e33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_MAJOR=14
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_VERSION=14.12
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Thu, 09 May 2024 18:31:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:31:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:31:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:31:12 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:31:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:31:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b675d45afe983b29c7135f33138e534ba9aca9ca6d05d28e546e09d1e6bba8`  
		Last Modified: Thu, 09 May 2024 21:59:43 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4f6c09ac2d383e82b8fba12dd71c915fd20ddea25bd838ee27c29df1a0982d`  
		Last Modified: Thu, 09 May 2024 21:59:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407922a8da7e91cb239fb04ece3b87af6f9ae690f106f4089e7feab5b08de8db`  
		Last Modified: Thu, 09 May 2024 22:13:09 GMT  
		Size: 91.5 MB (91535282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ec0e7854352d9ea6900641f6633f873fc7d3e88b03ee357b9787c364d46c1b`  
		Last Modified: Thu, 09 May 2024 22:13:07 GMT  
		Size: 9.2 KB (9206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97179d593ed113287b4ef60a23baa42d47029832046fe2ca0e742f0269cf51c8`  
		Last Modified: Thu, 09 May 2024 22:13:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3cb7e0d4c96fdf7c36d34b3edf8efbb5c700f375dfdb2b0308d6303743cb3c`  
		Last Modified: Thu, 09 May 2024 22:13:07 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85804c48ad1c27d9f955001f21625a9485de58718af6f505cdf2ed5f9a569c7`  
		Last Modified: Thu, 09 May 2024 22:13:08 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff48dda2ad5fd96776b1eaa89ab24985033bc64868afb6d52aca7fca817072f`  
		Last Modified: Thu, 09 May 2024 22:13:08 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:ec5cc1453d35c66161456adaad5b22c98d8a0923586776700bb3b51c9e1c4b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 KB (37302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f37b2d9ef05443461d8059991b4475b3c59b1afd3b351e5c6820412bf8c1ff`

```dockerfile
```

-	Layers:
	-	`sha256:91fab9741a7dab721ee131506174758bdfb68fa1e8c786726c062fca2df89be8`  
		Last Modified: Thu, 09 May 2024 22:13:06 GMT  
		Size: 37.3 KB (37302 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:535452f6cb61dc5f24829c5f8b1952e154376469a4cb0bdb0a6da34ecb655135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87426170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a432ba5d54f737970143792eebe067c9705f0b05d74899650cdc426ffa91bd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_MAJOR=14
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_VERSION=14.11
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_SHA256=a670bd7dce22dcad4297b261136b3b1d4a09a6f541719562aa14ca63bf2968a8
# Thu, 08 Feb 2024 19:28:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:28:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:28:15 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:28:15 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:28:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34183be10276d5bf28456f8dfa0b74b7d3728c5cf15e6e32a1203d02c80f06ed`  
		Last Modified: Sat, 16 Mar 2024 16:21:42 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bfc51b527ab2c0a5829fb7c7ccd2555218ae3b9c54fce2f19c92a88f06ebe1`  
		Last Modified: Sat, 16 Mar 2024 16:21:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f396efacde46e473e7129c4cf37f42e4a1e719fca87e60f85225fe60469736c`  
		Last Modified: Sat, 16 Mar 2024 16:43:05 GMT  
		Size: 84.5 MB (84490783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c105e61defd269b01c2960a9f43406f6d873d2cb8235516bf96b85dc44c7be3`  
		Last Modified: Sat, 16 Mar 2024 16:43:02 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20500fddbdf5f5fe1239d5c2c519ecf426b4d137f0a7383d9c19e0204308429`  
		Last Modified: Sat, 16 Mar 2024 16:43:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fe03f3d07a86b7fa53231c9eee70be2df1d68ad5ceb816b9d33334ded7872f`  
		Last Modified: Sat, 16 Mar 2024 16:43:03 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c70d4944b74870c10408abc2d24b9ee97588fb8e67eeb4d1b173d8e1d6a3b0d`  
		Last Modified: Sat, 16 Mar 2024 16:43:04 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc047d14a2584fbf7dd43da0552a0bb9fd06f8019febb01ba73d8c8935bc291`  
		Last Modified: Sat, 16 Mar 2024 16:43:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:f0271fb68257fdc45005693dfbfc43dd0a93221e4d86ea51a22be133fc4b5013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.9 KB (994865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36becdeb2358256a0a67251894fd35f1922be6f2dbcc4bb3648675e4493502b4`

```dockerfile
```

-	Layers:
	-	`sha256:9071b862abc2ecf3a0da9b4ac46951ff784c1f3038ab68e5bfdbee3498ab9c71`  
		Last Modified: Sat, 16 Mar 2024 16:43:03 GMT  
		Size: 957.3 KB (957349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aef6f6c98f92d9fa0ad684df50a88d55878b074a033b908878eaad9bc0fc78e6`  
		Last Modified: Sat, 16 Mar 2024 16:43:03 GMT  
		Size: 37.5 KB (37516 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:b704f2c1a0b8b3031f145f3ee944fa4cdcca41bf1a0ef3a66df3a70f8cf910e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94903743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ea63eaff4818d6a89b3723929f3ef7cf14e3cb14d85c9a5f75362fe44e8bd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_MAJOR=14
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_VERSION=14.12
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Thu, 09 May 2024 18:31:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:31:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:31:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:31:12 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:31:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:31:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6426790b86128c81359671377728ac209ddd73d25d62a98505f61e0f34e541c2`  
		Last Modified: Thu, 09 May 2024 22:23:47 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2765e6e641bc36e3e37080f48cbbeb6eb6beb085e0a5cc4d749578ec2b27d79`  
		Last Modified: Thu, 09 May 2024 22:23:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06042dbb507e00f914d8604a261e1b1f2526522f345222745ae6b2ee40808598`  
		Last Modified: Thu, 09 May 2024 22:39:07 GMT  
		Size: 91.5 MB (91539543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9036d8625308f3826db6d92baccbb96aab402e7164b27e927a1ca187645c0940`  
		Last Modified: Thu, 09 May 2024 22:39:05 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4e5f5618881bc83fa81e8c0cc4938ce6afaa5cfa27c90301503fbec772b688`  
		Last Modified: Thu, 09 May 2024 22:39:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e6606ffbd6b44043b71d4c0a9625a6b3cabaa8d8353b30cc4e4def86ae66c2`  
		Last Modified: Thu, 09 May 2024 22:39:05 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb6bfe745c6678a8368ef9b0f0b044eaa6d38331bac6b9044e18827c89a67f0`  
		Last Modified: Thu, 09 May 2024 22:39:06 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190c5164dfbefae3c456aaed4993e5b6b4f23ba5f6d03460ea83e6eb5523a63c`  
		Last Modified: Thu, 09 May 2024 22:39:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:a05c7de9d5646c88f03b1eafcc80b1d7772fef60a969ff2ef33a337dd8c9197c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.7 KB (994710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93ff5ced05817247d5a235987a57767b92b18477013e3d7829a89ac0808f122`

```dockerfile
```

-	Layers:
	-	`sha256:4665767cf8ccecd45da4a25cd176a0842b235268f8b1e9cd14a19e00ee3151bf`  
		Last Modified: Thu, 09 May 2024 22:39:05 GMT  
		Size: 957.3 KB (957328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2bce73dd0322923624c9e0991b6b0e71d474882110db77d15778c0262d14a1f`  
		Last Modified: Thu, 09 May 2024 22:39:05 GMT  
		Size: 37.4 KB (37382 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:6eb065454e35f2669c8311122e0180bb0f5a02f69995a881446ab06f799f2cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101362462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e355ce87b95279473b7918959b558881b3b5ff1da2adc03a55e63bbfa4ea48a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_MAJOR=14
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_VERSION=14.12
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Thu, 09 May 2024 18:31:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:31:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:31:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:31:12 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:31:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:31:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca65718f1da8e5c585a6d58ca2f235d34496cc88dff975cab0f79c39db27020`  
		Last Modified: Thu, 09 May 2024 21:57:20 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bf0dbc4a38c8026d931728a4c992ec251a58a07e2942a1812eb9d730ac637c`  
		Last Modified: Thu, 09 May 2024 21:57:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d00ce1344fe6ab5ea6375e25b3cc52a8411d4db85940c2a488231798e80d916`  
		Last Modified: Thu, 09 May 2024 21:57:24 GMT  
		Size: 98.1 MB (98101887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461d1e9e88bd2e8af7013b65b5808e1af1198867b42f19753b37d1c08b5b66f9`  
		Last Modified: Thu, 09 May 2024 21:57:21 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb222ad156a4583184862324272001d2f6352b8687c1b024302c46700af703a9`  
		Last Modified: Thu, 09 May 2024 21:57:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366d742726bb44637fa8c237561e6d9f9553cffb7d213c65f32119acdc693044`  
		Last Modified: Thu, 09 May 2024 21:57:21 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1c3d8f77421f51a235d13b1dc8d4536135edf950ec6e3c9d0b00b3cc11ab67`  
		Last Modified: Thu, 09 May 2024 21:57:22 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934d9c2340ee74ca8df68685efe6de635a52a4f7a86eb4afc67a0eca18bb1dff`  
		Last Modified: Thu, 09 May 2024 21:57:23 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:47a07338d17cf93b76e588e71d38b754b5fabd88e0678d690693102b5d73fc13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.8 KB (994789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e913c3c7526974a0d033b36babdc4ddf4556131324266e6afab1e676f3abf73`

```dockerfile
```

-	Layers:
	-	`sha256:b18ab046b2ecf981e128d03d15895f424a5330d4c9e4f07ad7b1c570100af940`  
		Last Modified: Thu, 09 May 2024 21:57:21 GMT  
		Size: 957.3 KB (957292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b05143f0731d87b5a45a153d81a1bfd2676260666778057af0b885e923ea062a`  
		Last Modified: Thu, 09 May 2024 21:57:21 GMT  
		Size: 37.5 KB (37497 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:d48c83ca7156cbb5fd0352bfffd95605a78860707ae4e30a5f64c38a4dbab7fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.7 MB (98737526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33e42a7d9eaec744282a5c492890984b098d99cb3538f6088d5b08679917870`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_MAJOR=14
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_VERSION=14.11
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PG_SHA256=a670bd7dce22dcad4297b261136b3b1d4a09a6f541719562aa14ca63bf2968a8
# Thu, 08 Feb 2024 19:28:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:28:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:28:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:28:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:28:15 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:28:15 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:28:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79df8127be221428a326f357e04f1c6c7907b2ac1145408ba7f22a36fe89ce2`  
		Last Modified: Sat, 16 Mar 2024 10:37:24 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e0b43ea44af8adfb383299b0e1e2f4fdbb58b567f44792024513de6b0a73dd`  
		Last Modified: Sat, 16 Mar 2024 10:37:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d05a23be8a7265ad95ff229bb7d8dbac15604a037f5b834dad428cff138008`  
		Last Modified: Sat, 16 Mar 2024 10:49:34 GMT  
		Size: 95.4 MB (95362691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b09de0abd10549296474da61a7c54c9d88ab26e156b23cf524af03c31044d8`  
		Last Modified: Sat, 16 Mar 2024 10:49:31 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed25a8937726998b4d4e64295ef11f3d7d814114c24687da156b1fe71baa05d`  
		Last Modified: Sat, 16 Mar 2024 10:49:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fa6415892592f2fc44af93ee0b4f04eda306fa047b368e646aeeae4eb1fbd5`  
		Last Modified: Sat, 16 Mar 2024 10:49:30 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85790bac9a89fe189b3aaffa68aef1f1643306b97e565f46028027bfb8455625`  
		Last Modified: Sat, 16 Mar 2024 10:49:31 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d0fdef3dea46bde17034c9014afa87bcfd9ef165588d18d57bc7d15196f4d8`  
		Last Modified: Sat, 16 Mar 2024 10:49:32 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:117a12f2d7d4c0349aeff0998b0f152cdb9745d93720365812ba766f86026888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **991.3 KB (991291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa0868ec609ec0b45a3616f060d79b8cde9418a72624135a830cc42b6b79888`

```dockerfile
```

-	Layers:
	-	`sha256:1e4eff32d7fedfa81fddc6415b506c0f74ab5678684dc47d9cf1b47be461d4c5`  
		Last Modified: Sat, 16 Mar 2024 10:49:31 GMT  
		Size: 953.9 KB (953872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b05d3ae2b0a25299939c0d238d011e17bf69066947cdb66add8aa8bda7e89fd`  
		Last Modified: Sat, 16 Mar 2024 10:49:30 GMT  
		Size: 37.4 KB (37419 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:4058e0f9ad7f24fe0eca46b28e98867dec6b70bfd9150f07f923e38c3d1d9c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104905300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a1595be16da244b750bfa1365a72374f84b9bc2a27eeb3bcd7d88402a69549`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_MAJOR=14
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_VERSION=14.12
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Thu, 09 May 2024 18:31:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:31:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:31:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:31:12 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:31:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:31:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5640c2be82ac04ba5ddac695379fa624aa02fd3579b534fff1c3dd4eba189313`  
		Last Modified: Thu, 09 May 2024 22:13:40 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85541a3a0f2695e7b89ffb03367e1f86a74f6ff41d24e68ce35f629a057ca65a`  
		Last Modified: Thu, 09 May 2024 22:13:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa63d39b23fe28b9b9b7169dc568ce753338c63784271c0b1f5bf0a27b85140d`  
		Last Modified: Thu, 09 May 2024 22:36:11 GMT  
		Size: 101.6 MB (101646172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b8e1fb7bb2c70e078002871d219bf3f7d9a00227ac04d5f3d77b4b518d206a`  
		Last Modified: Thu, 09 May 2024 22:36:09 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827cd3dd7a6b24cc4b67e61af70b9c216c94a649e595b9c8696382ed5994c440`  
		Last Modified: Thu, 09 May 2024 22:36:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ccb3a99f2117ed7a86dfc65fa439d4c0e983d0ff8c58026e5a8e6e6a6b854d`  
		Last Modified: Thu, 09 May 2024 22:36:09 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc81717685133d990c912035eb178c125823b5565c54ca16d471721c9b5694f`  
		Last Modified: Thu, 09 May 2024 22:36:10 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699ceff85b3eb09d9034bbd485ca25944752484b8bc47079d8a530baa0a149b3`  
		Last Modified: Thu, 09 May 2024 22:36:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:187863a2e3edfe8a0167da734165b2f452025b02bd5c909ccc38620c39a301cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.7 KB (992742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5c2f369210a1fd151933af5b954ab1d32d6faea0ed7c4137b4aabf58d50e9c`

```dockerfile
```

-	Layers:
	-	`sha256:e559746db52ce91b7cc4b33b9723c100c690b3275d448a15782904f333162764`  
		Last Modified: Thu, 09 May 2024 22:36:09 GMT  
		Size: 955.4 KB (955363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ace1c73a3ac87b2d7e3596aef9d47729a1c028b5f7aa1006b74c54169d9954c1`  
		Last Modified: Thu, 09 May 2024 22:36:09 GMT  
		Size: 37.4 KB (37379 bytes)  
		MIME: application/vnd.in-toto+json
