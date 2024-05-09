## `postgres:14-alpine3.18`

```console
$ docker pull postgres@sha256:9393d6917530f3b543bb81a3dd5284bce51a19523d242a643b0fa4e5135845bd
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

### `postgres:14-alpine3.18` - linux; amd64

```console
$ docker pull postgres@sha256:af0899d0a2a619cc2724e32fa0211e0e2c233f957ae04975b919125f19978e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92736613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01785a4e8dc20570fcc4623f844910b98bdf75ac6a2c82b44371c04179db5012`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
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
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efd4118c79439dd0f0077fbdd972703f469692a466a6da0c19e83f8bfcd8d7d`  
		Last Modified: Sat, 16 Mar 2024 00:00:38 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c39848facc451bcbda1608df90e9bb62709685c3c6d74144474e59bb151d49`  
		Last Modified: Sat, 16 Mar 2024 00:00:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e6085a9739ee2f77abeb781734e6bd59adf5a23c8246cf7c6ae49353be20a6`  
		Last Modified: Sat, 16 Mar 2024 00:00:46 GMT  
		Size: 89.3 MB (89317589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d236fe00812d021b3c592c63681b3da8ebc2655d8cda1200df098322f05c1af`  
		Last Modified: Sat, 16 Mar 2024 00:00:39 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3103b43d5d8f1f1277574c33761eff828858ec9aa2f9ddf0f08f721b38c57b`  
		Last Modified: Sat, 16 Mar 2024 00:00:40 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6676b37c30fd84e7bd66c63615f50b49d3290c7ca0aca7b468613d190dfd11f4`  
		Last Modified: Sat, 16 Mar 2024 00:00:40 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6938905c34df07e2d4c34f0d9cc0a43474e1db23027bdd48faa21df8f37c098`  
		Last Modified: Sat, 16 Mar 2024 00:00:41 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44b53db3af2191f542f91249cb933f1f0a9df375628512902da050dc9ef767e`  
		Last Modified: Sat, 16 Mar 2024 00:00:41 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:917c2c18c949571080f68b0c8277893fb6bea749367de664c3686f99d63afa89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.0 KB (992984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d357f77644231cbc5d3444420c74290eef551cf3bc54e64bcff5c0bb909825e3`

```dockerfile
```

-	Layers:
	-	`sha256:8a072fcc1a82b0241ec59f5be6d4929db21c52b707a692696b94494a5a562751`  
		Last Modified: Sat, 16 Mar 2024 00:00:39 GMT  
		Size: 956.1 KB (956072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fc770c8552696a91c2faa9ebcad96a2f1a3788c393c69f4a348225fd35342a2`  
		Last Modified: Sat, 16 Mar 2024 00:00:38 GMT  
		Size: 36.9 KB (36912 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.18` - linux; arm variant v6

```console
$ docker pull postgres@sha256:246787d8e3ce72ff80fd009ceba3e6de6e19e9d9f24c00256a18eec6ac63283f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93213516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87cd8f17fd635fa681ed683908f271b38272b3762683f8c35446ad498c9b153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
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
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a108ab915fc8c9e416a781c5a7bc761154864183018326b62496c9ab46c866`  
		Last Modified: Thu, 09 May 2024 22:03:00 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67939ca05ee3b2791aa4415e0f9cd611de6318af5254b1813898bcbd5a17f6b5`  
		Last Modified: Thu, 09 May 2024 22:03:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d372fd6e6e715f19dc406a0021bde41855ce2e494018bc176e64c035e50e8f7`  
		Last Modified: Thu, 09 May 2024 22:16:21 GMT  
		Size: 90.0 MB (90049971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b8cda12b2e1453b66c5afeb60afdd3390a13c92947de585d1431bdd85d7c8e`  
		Last Modified: Thu, 09 May 2024 22:16:14 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb3f6a6a784cf0efcc6531080867cff612d6228f04349fd520eeb343539b530`  
		Last Modified: Thu, 09 May 2024 22:16:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a940dcb572e7be7e07f384cd02078a21dc2f065a3b30ad9f25ebd96c5454c285`  
		Last Modified: Thu, 09 May 2024 22:16:14 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a5873ae2793c251d73cf65a9a462e665b36a0e6ab610655de7c1b80ad08914`  
		Last Modified: Thu, 09 May 2024 22:16:15 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8759880b0edd560b66d14653748dec6945ee9de0cda699cf321b37146264c8e1`  
		Last Modified: Thu, 09 May 2024 22:16:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:b3a9a34aa51cd54e7c608b7549decbbc1dfe2a7e194bb836b49a60172c237044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 KB (36664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab4e1f1600b89ddc33991cca7552100b0a796ebf1cdee90219c2ba768dbab5f`

```dockerfile
```

-	Layers:
	-	`sha256:f8db6938dc8d7139a8f86b3249f2509981e63af957c6cc56f5c35a498757133e`  
		Last Modified: Thu, 09 May 2024 22:16:14 GMT  
		Size: 36.7 KB (36664 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.18` - linux; arm variant v7

```console
$ docker pull postgres@sha256:7d99dddd43d6d3fae4e42819756553ca334ec1cdc81063ab32c4363dcd4e6d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86118325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2fe9491a045763ec22440d3a321d15ac64dc0ea719fcb26234601520834e89d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
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
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd951a98e9bc26ad55202a730fbf176a99a4f1dafeac246adac9b93116e6841`  
		Last Modified: Sat, 16 Mar 2024 16:26:55 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83b4bffee9860001c77fb26ccc9519a32dcc2324e1b6490008d4eee80c0ab7a`  
		Last Modified: Sat, 16 Mar 2024 16:26:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8e1b7aababddf8e1ddf19de473545fd1a671ec182f4783bce4f709051f0773`  
		Last Modified: Sat, 16 Mar 2024 16:48:31 GMT  
		Size: 83.2 MB (83200449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1311611a91fd87c36619af7b2321be5866e2845d6a4e97eae48da6964f7cf27b`  
		Last Modified: Sat, 16 Mar 2024 16:48:28 GMT  
		Size: 9.2 KB (9201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d5c6922a341406d98186aa5fcaa3e1c54540e779ff00985e8fd5642a172156`  
		Last Modified: Sat, 16 Mar 2024 16:48:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c6e9bec6f1adfdea26530850d8b99568032af6d1f974e59c4b67bd3e092723`  
		Last Modified: Sat, 16 Mar 2024 16:48:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca7d6bae615b6dd3edf2b5fce956c6446aff0f902656db05de7535b2ea39b48`  
		Last Modified: Sat, 16 Mar 2024 16:48:29 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722a53ed761842793ad765a32ce1980c818a3801871318bb3e95731e47acf5c5`  
		Last Modified: Sat, 16 Mar 2024 16:48:29 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:4b5d0c2906ae8b4bef5d43e03542019101215b306ff0198a8ff0448dd47b3e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.0 KB (992971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0947554b97c7dad97049a53320bc72d461c38347b8b9ad1b1c49f7dc33dd5b4`

```dockerfile
```

-	Layers:
	-	`sha256:dd1c2720a9528350a6bc5d75b1a49853e379532a8ad663864556d704781194e6`  
		Last Modified: Sat, 16 Mar 2024 16:48:29 GMT  
		Size: 956.1 KB (956092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:565c2c124297f19443435593ab7f7e0c3cf54824ddc2b9ae236ddba4dd5e4cfa`  
		Last Modified: Sat, 16 Mar 2024 16:48:28 GMT  
		Size: 36.9 KB (36879 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:daf1d9a147cc19bfba12f51793be246dc1068d334457c0751ca54f86905f6399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93669439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3174724d0859064e7a91cbda07bec656ae2af749d8564882c75bd52478b5797f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b240be4b3e5ec1e8dcb9ed310937046e4279e0fa6616a6838631e3652dfe15c5`  
		Last Modified: Thu, 09 May 2024 22:26:25 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8682ae92e29385ff5d6f1929c06e62fdf846fcd1d301154ad1747043bee37f21`  
		Last Modified: Thu, 09 May 2024 22:26:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63244f250338d74a8394f3a8d44d2eac1446019579e8ea5c393964d5f7e50101`  
		Last Modified: Thu, 09 May 2024 22:41:35 GMT  
		Size: 90.3 MB (90319596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f80724517c0f03fab0d125a9d5ac861d35c8e8bf75e5d5471569be893c48cb`  
		Last Modified: Thu, 09 May 2024 22:41:32 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cdf3b42cd129c2b8a86a540fdf72957cc3af38c01a658c88697a7bcb2bf09e`  
		Last Modified: Thu, 09 May 2024 22:41:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e814b0525faf0c657108f1ea76d04ded6f1a6f5266ee307ec475c3345e34f4d`  
		Last Modified: Thu, 09 May 2024 22:41:32 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e8d2894c06e8a83140b4d6edc9ace674e3acc38c59ae81fa1004ea9471b39a`  
		Last Modified: Thu, 09 May 2024 22:41:33 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdac8136798fb0ca73685b4c0dda73fc7e3ef26b6c907615c03facbb7a9bf98`  
		Last Modified: Thu, 09 May 2024 22:41:33 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:315927d02177b4633496fe7e74b5d0d99129dadcf1ea69c059d76de7253a0fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.8 KB (992840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3142af740e32f012a6eb15c7b0fe25e3b05f936a8e0d9ddab042cec27fedf7ff`

```dockerfile
```

-	Layers:
	-	`sha256:c0bb9e66c2cba7c1ac9ae972979743c7fb81d1382c691042da10801492306d92`  
		Last Modified: Thu, 09 May 2024 22:41:33 GMT  
		Size: 956.1 KB (956083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4af84df8e5242a00b101957884a7200f2a6b35b1016b2623db691d33f69406`  
		Last Modified: Thu, 09 May 2024 22:41:32 GMT  
		Size: 36.8 KB (36757 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.18` - linux; 386

```console
$ docker pull postgres@sha256:d94b9ce126b41439d6a53284158a600c12c7c7b4f17d77594f2fad9630c834d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99632406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840ef07fca74e97289b72400f2e97d4b90bf8bd94d7c9218c1bf143381bdeeab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
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
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062765a8a012c2b4c4e8710a4befe070c5d2b7c8a0a809bc82a3dff336e096c2`  
		Last Modified: Thu, 09 May 2024 21:56:59 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31792a01b7ade07f8be2b8c23ef2b117e1512456070ff28325464cb54e37ea7c`  
		Last Modified: Thu, 09 May 2024 21:56:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0068ee0b6d7d35070033658a9b48412480b5f75fae731f52b554cb34d9ea87c`  
		Last Modified: Thu, 09 May 2024 21:57:01 GMT  
		Size: 96.4 MB (96376854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f696b340bdbc02da4ca2457b5e38ddfbe36f93a35ec8af233d14fbbc1be4bc4`  
		Last Modified: Thu, 09 May 2024 21:56:59 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbdad877fa6f75d774114d29157b044a1ae96b7d8a8d5477d027ec3e7d849c8`  
		Last Modified: Thu, 09 May 2024 21:57:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eab4cb68746ef941129b05a6396d8070aab458ac9ebd1940e42cb753bd1dda`  
		Last Modified: Thu, 09 May 2024 21:57:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c51646867f192ea20832ebcfa4954e2fabc371b5e04aca547c31caf11077f6`  
		Last Modified: Thu, 09 May 2024 21:57:00 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59fca5883040ac62fcb1c665737c716eec0dfb86b0d6ad9c405a8b68af8a922`  
		Last Modified: Thu, 09 May 2024 21:57:00 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:1f9d127ea3463f1ec4a0efec6b14b8ba949ecee2c20361b5c8eda883df2581fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.9 KB (992947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af12768496bb36e7be3be9fb86fccb4887d6ff38e5e0cba72d0e4482bcd244fd`

```dockerfile
```

-	Layers:
	-	`sha256:892f2d9d4c0fa20026736015440f21f591a8fab4098948e308fb28c6f8bbbe1c`  
		Last Modified: Thu, 09 May 2024 21:56:59 GMT  
		Size: 956.1 KB (956061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0edf0d79e7a0274bb66bdc4fc526ae12a86aea2a3fa4e2b7676fe310c407a06`  
		Last Modified: Thu, 09 May 2024 21:56:59 GMT  
		Size: 36.9 KB (36886 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.18` - linux; ppc64le

```console
$ docker pull postgres@sha256:bf9ba56d0ba9304ed7ffa080ed66b827599137da77f41d596d5cd206f1fd05b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98389089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8012198b01161630ebacaaa91b4d347265e308431a004ae80d951706c0db84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
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
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bf06424f58ac7307d52d4ae986fc96c03d14c3e8c9546673273e53c183a35a`  
		Last Modified: Sat, 16 Mar 2024 10:40:30 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545ceadfd5057505b4e5d6cd51ddf57b0cb73f291f5b2ab2e392c78a73f6318c`  
		Last Modified: Sat, 16 Mar 2024 10:40:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b42451a988bcf3daa30129f2023cce3698d9453bca01ea30c867387e0dfd542`  
		Last Modified: Sat, 16 Mar 2024 11:04:24 GMT  
		Size: 95.0 MB (95024118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e98ebf18c874ef665f315fda9e5604be273e7b2d1fb8b332fe72028fb58097`  
		Last Modified: Sat, 16 Mar 2024 11:04:21 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d860d226e82f2c76d7f6931e98ef044dab6cde3cfb6796af565fe3fb906fdc2a`  
		Last Modified: Sat, 16 Mar 2024 11:04:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d856988651499aea0471ecc1bf89107b8bada499d6dd32a2cf86780347c5965`  
		Last Modified: Sat, 16 Mar 2024 11:04:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63fbe404b406e6e17987740c414a22e6428ea4b4c3e23c495a14ee89003be89`  
		Last Modified: Sat, 16 Mar 2024 11:04:22 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e3dd439ee78bad14ef93a1737036250b9152f2ac4a04184fa404d6ae39b23c`  
		Last Modified: Sat, 16 Mar 2024 11:04:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:4fed043c633aa78915d987e3122606ad288cb785ee1670598cbda39d0e5e3b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **989.4 KB (989404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e78f68276f92a6e8dd6dcc8176a6aeff4d6af35b9979d6a6e1637f056cab355`

```dockerfile
```

-	Layers:
	-	`sha256:10d5380be028cdbdcd1edaa144ed9ff4a533ddc270acd8a08db739c9091f054c`  
		Last Modified: Sat, 16 Mar 2024 11:04:21 GMT  
		Size: 952.6 KB (952619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:293bd13e3805641ccccedffa46a697afbb9329120851b14ea779b20435f3025b`  
		Last Modified: Sat, 16 Mar 2024 11:04:21 GMT  
		Size: 36.8 KB (36785 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.18` - linux; s390x

```console
$ docker pull postgres@sha256:5edbadb892d7ee3a5c8abee3a3e4cb37a3d06eb77ab513c10330391a60e6de0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96233340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5fd21a246feec25ddfc16a003e3ad460d0af2ec355cf543e747814e3f84135`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
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
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7673a4910a6fe9d042a53154b0dae00bc60a57223cd10a184ea7a99d82bd0cc`  
		Last Modified: Thu, 09 May 2024 22:17:47 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2a19d1c8865ecd491b02ece010add44b02f480a09889be228a72bd65e790fd`  
		Last Modified: Thu, 09 May 2024 22:17:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42de5aec9859d05ff0ffdf0a875d375c2f56975408260e07c55258091120b929`  
		Last Modified: Thu, 09 May 2024 22:39:31 GMT  
		Size: 93.0 MB (92999324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a837bf1b68b2dff926e33d250f34275125ad028c5e1a2aaeff6079979238a832`  
		Last Modified: Thu, 09 May 2024 22:39:29 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865c36222f32f223192d8f781fd5a65042d3c2c794075610bcbaf595a5ce5153`  
		Last Modified: Thu, 09 May 2024 22:39:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58017e59a400a5b5610e5294d6b7d9bbbb0216857f27e00533b367b03f6bc5c9`  
		Last Modified: Thu, 09 May 2024 22:39:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d5a75c6777df8a8b8c663d5cab929a56b18de8471bf1297e36ee4512157cc2`  
		Last Modified: Thu, 09 May 2024 22:39:29 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ed0ea0475a9c2ce3427b6bb6ec41aec278240bd74fdda2b6514deede12f5af`  
		Last Modified: Thu, 09 May 2024 22:39:29 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:f140539389231cb55730c364f68ba56efc53caf39adfdec73e4b0b7c5ba397bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.9 KB (990873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b16495041dfc4b025235f641d1b107c07d6cd473198793cdbfec4f4130c2f18`

```dockerfile
```

-	Layers:
	-	`sha256:34152b80bf7d0f43079a6cd27f24b5cc69ff5fe7dc10e8b47aaf54936c679016`  
		Last Modified: Thu, 09 May 2024 22:39:28 GMT  
		Size: 954.1 KB (954122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7003f4cdc1f7583c62c8a355a61ceb8b7326ecd088cddf53d8e8d9f9fa188d78`  
		Last Modified: Thu, 09 May 2024 22:39:28 GMT  
		Size: 36.8 KB (36751 bytes)  
		MIME: application/vnd.in-toto+json
