## `postgres:15-alpine`

```console
$ docker pull postgres@sha256:624938150564895912e8226a94646e4732d5d7e6202ef4dfd50b36ab29dc4d5e
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

### `postgres:15-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:7ae6db0653c818b70138e2dff9e164b24e650fced035847633cd28a0c21f5350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94821839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478703aef7f8676f16cb204389b751a26df4b85015e4d986aece4314ed13935c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 22 Dec 2023 00:27:15 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=15
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=15.5
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=8f53aa95d78eb8e82536ea46b68187793b42bba3b4f65aa342f540b23c9b10a6
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 Dec 2023 00:27:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
STOPSIGNAL SIGINT
# Fri, 22 Dec 2023 00:27:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2144f32fb020c5065622b631a7ac2e569319ede7b070a687dd0c0055912c8cd0`  
		Last Modified: Sat, 27 Jan 2024 00:57:27 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae5880a99925721feaf31e049da854509fc9b2f6c5f1fc14c56c934744fe3b8`  
		Last Modified: Sat, 27 Jan 2024 00:57:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7e005279ff39cc3888067813d9a2afa357a829548466f93e1236dd9df482d0`  
		Last Modified: Sat, 27 Jan 2024 00:57:28 GMT  
		Size: 91.4 MB (91396382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7c8daccf63e2fce47fe5e4d860a1aab7d259a21ede996aacfe62e49808ce81`  
		Last Modified: Sat, 27 Jan 2024 00:57:27 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c99ea33aad5f1185d6e64637466cb64225f0c0a66fc8190d996707c6c761aa`  
		Last Modified: Sat, 27 Jan 2024 00:57:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994c5565273a48fe6e8c4c182b2e1b3cd440fc3cfa8389c7599c0b15db25a959`  
		Last Modified: Sat, 27 Jan 2024 00:57:27 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad00cec9913423f5e51295d48b3bb486cc0989cf6c2b255d76e37c2eb59b896f`  
		Last Modified: Sat, 27 Jan 2024 00:57:28 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986bbf9a3bf6d3a2f707b240442e6c10cffd002d35c7ec42c4b8b56250d6f043`  
		Last Modified: Sat, 27 Jan 2024 00:57:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:7edfbcfd3ac61cd350dd0be380b07acd8e042de54181f7c36d7500e438a1e022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.2 KB (845162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecee1751a700305f8a9683d8f2a793d8fa3ff66c43fb721520987582256dfa68`

```dockerfile
```

-	Layers:
	-	`sha256:483250fe5b9fc8ff3c93fc147445a29da1407af5f32a0816a5a4a13d7834e5e0`  
		Last Modified: Sat, 27 Jan 2024 00:57:27 GMT  
		Size: 807.3 KB (807317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c03ad6f2ddcac3d8442516252185e07031d42e241e66195905def5946e3d755`  
		Last Modified: Sat, 27 Jan 2024 00:57:27 GMT  
		Size: 37.8 KB (37845 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:9360df70a0e8a7393adf309d1f13f8b5d1e5394b4dca9a85452bf8520cdb7e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93596723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d5d16b4d9de3fdc402f761d67339c66884ef6ed50eb8f6e0f11faf6250f277`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=15
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=15.5
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=8f53aa95d78eb8e82536ea46b68187793b42bba3b4f65aa342f540b23c9b10a6
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 Dec 2023 00:27:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
STOPSIGNAL SIGINT
# Fri, 22 Dec 2023 00:27:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b8fa596712ea779c4cb87ad98b3ad730138e4b5d96f64ec23a93cc60393aee`  
		Last Modified: Sat, 06 Jan 2024 11:54:19 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c59b03b6f5155de1f45d96c0cd184b8faf805859e9ea5a1eb7bb6cf3d2c38d8`  
		Last Modified: Sat, 06 Jan 2024 11:54:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6551b301b5ea15a54d95b60ca27f671a9c3c840cd094ea0c2808c6592bd6a387`  
		Last Modified: Sat, 06 Jan 2024 18:12:00 GMT  
		Size: 90.4 MB (90414846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a35f13c2346cd24e9233e7e4abdee7e986e16dc399fe198253e658bda2ca55b`  
		Last Modified: Sat, 06 Jan 2024 18:11:56 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee8f5158d3bb44f62ab9a26b56e6c22750f38c465e764df428cd15f14fc1451`  
		Last Modified: Sat, 06 Jan 2024 18:11:56 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914d76564cf711090dbef6a93ee64a2a3c775e67403589027e032edb691189f1`  
		Last Modified: Sat, 06 Jan 2024 18:11:56 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6883d12776a82308457ad9a90d3133499a23c22133fdddc1905b3c1e11057ee6`  
		Last Modified: Sat, 06 Jan 2024 18:11:57 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61a6c93bbc19abbd6c29da4d061f4a5330bcc209ea55f6c6ca453bf51785824`  
		Last Modified: Sat, 06 Jan 2024 18:11:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:a862ae95d879457f79c18e6bc18eb2c917990f793f3f2fd3940e9a5213112d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561a3834c660724d8edf7902809d10f7128c4425667fad3944ff9b3331b1b4fa`

```dockerfile
```

-	Layers:
	-	`sha256:65eab90700fd43b347ae9d817457ec4ce45291f6d1973f352d0960ee385c424d`  
		Last Modified: Sat, 06 Jan 2024 18:11:56 GMT  
		Size: 37.6 KB (37612 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:a61bac295e7ac77ede16b5bcbc79725d9c8060fc9630d0553e0d3f6ffc3ec8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88051124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc75983cd9acfff4fd2603e45d083c6f88d67846e60a7b9fca86849a9cb545b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 22 Dec 2023 00:27:15 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=15
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=15.5
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=8f53aa95d78eb8e82536ea46b68187793b42bba3b4f65aa342f540b23c9b10a6
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 Dec 2023 00:27:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
STOPSIGNAL SIGINT
# Fri, 22 Dec 2023 00:27:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf782f407230cde68ad1fe94a87a82f2ee6564456dbb2e632ed6b9985a758725`  
		Last Modified: Sat, 27 Jan 2024 16:43:20 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab3bf70fcb637ceab1ecc0f8ba4e3d999807b3d3f99729e8585e51cbf9a8b7f`  
		Last Modified: Sat, 27 Jan 2024 16:43:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c360368d3f08a4127338e7e83def63286590e5d8df365e2f9b9e3f41fdb2a9a`  
		Last Modified: Sat, 27 Jan 2024 16:54:36 GMT  
		Size: 85.1 MB (85115498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c3090d6d5a0abe9da821108cfbc19df996dd8b2d246b792660f7d699a6cc52`  
		Last Modified: Sat, 27 Jan 2024 16:54:33 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9491fb959d50e6ee2332fb1b139a53d3eb431eb4f823c2937d991596eb602c24`  
		Last Modified: Sat, 27 Jan 2024 16:54:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5471b45d86bdfd2307a25758fbc08402b7f4d9b57f09b23d4c9fdb1b9052ab98`  
		Last Modified: Sat, 27 Jan 2024 16:54:34 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3434d149de458a18a4f96c0103f9b1f7804db8e48e865609821c07875f1e600a`  
		Last Modified: Sat, 27 Jan 2024 16:54:35 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa196431e549286b1f7cdf52765bacb7e8dda4c9c810709c5ea6ff568acec79`  
		Last Modified: Sat, 27 Jan 2024 16:54:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:ca59da9eab05d34a8dc15635765232ebeb618f70e75b18bebbc2438514cb5f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.2 KB (845180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f5c5bfdb53841e4a7df778d55c36e3d0dfa5908c5244277410fce13a1674b6`

```dockerfile
```

-	Layers:
	-	`sha256:6be5ad248e07eb9ae2622a05c22b7b2ec104c703de129a776d507355afa60f81`  
		Last Modified: Sat, 27 Jan 2024 16:54:33 GMT  
		Size: 807.4 KB (807353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4eab89fd3741deedc32a0138e9a7909583bd152a066a90a336f9f94d9e1ffc84`  
		Last Modified: Sat, 27 Jan 2024 16:54:33 GMT  
		Size: 37.8 KB (37827 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:9e46fe84c51fd035c8683014e227eac4fdadbce300d7269aad98b87c70d4363c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93588098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440ffd2787846775ebc1e5f171bb709371dffebb0a3ce4b166c87b67eaab0336`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=15
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=15.5
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=8f53aa95d78eb8e82536ea46b68187793b42bba3b4f65aa342f540b23c9b10a6
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 Dec 2023 00:27:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
STOPSIGNAL SIGINT
# Fri, 22 Dec 2023 00:27:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a13ecc88456148cc73b8941875af2463232293d6e48313a5d057f52f188e04`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01277bc8c6d336069acfe7e4b99842b4e64eb3c6b65bd1dd31d3a6a8a1d98b16`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eee02989f6306e22575ae35b0f07fc29d52c4ac074afa51b91c0608509cab2b`  
		Last Modified: Wed, 13 Dec 2023 03:40:14 GMT  
		Size: 90.2 MB (90223569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ead3ef10950588847b35c2422f2e79430c9c30618f23ccf898c1beabaa89934`  
		Last Modified: Wed, 13 Dec 2023 03:40:11 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27916a8624f2c01c9cc2fab3cdab404f776562bf917d405c50ae4cf33211ebc`  
		Last Modified: Wed, 13 Dec 2023 03:40:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1130d561c76a7c6e598d18a45b0e4442930468989963b093945b788600f9ac`  
		Last Modified: Wed, 13 Dec 2023 03:40:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6af12413b87499c7113194ac2642eeeb8ba80ca1fa7bd5a6b7ad2cdea7f13fd`  
		Last Modified: Fri, 05 Jan 2024 02:27:34 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840cc31274eb0dfd436b79f441b358b970929b97cdfcf702395cfd733478f892`  
		Last Modified: Fri, 05 Jan 2024 02:27:34 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:dcd12c22356e26e3a4a039c8377525dbb3ce049ca67b58065c4ceda62b4e5342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.0 KB (845011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f308d7374409c602a8d4a115debb5dea9aa57fac1df3462bdc9a73ba821c21d4`

```dockerfile
```

-	Layers:
	-	`sha256:426f06e2122434c4f45c37dc5f11165cf422da816eb1785055e118b2c131ba56`  
		Last Modified: Fri, 05 Jan 2024 02:27:35 GMT  
		Size: 807.3 KB (807322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5af935284e99ec4de5fbad9656e7162f5c3ef5f3f2020e179fb1507e91cccf5a`  
		Last Modified: Fri, 05 Jan 2024 02:27:34 GMT  
		Size: 37.7 KB (37689 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; 386

```console
$ docker pull postgres@sha256:4f93531469f4b0c0fe98a52f9cc36b238d99469750738d5b20734358cda4eac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100130779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c131aeab51d745ef9fd56d54eba2d5f646e96a0db0b0c4eaccb672989373334`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 22 Dec 2023 00:27:15 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=15
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=15.5
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=8f53aa95d78eb8e82536ea46b68187793b42bba3b4f65aa342f540b23c9b10a6
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 Dec 2023 00:27:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
STOPSIGNAL SIGINT
# Fri, 22 Dec 2023 00:27:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc13f96bfe919aef9afa1a9c125d8b90bf3094892b352e3ca31fb43029f78ed`  
		Last Modified: Sat, 27 Jan 2024 01:58:25 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56311d723e2987a7b51329c7b4fb14ff0a24546eb32c0eea37635287a1805063`  
		Last Modified: Sat, 27 Jan 2024 01:58:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ea73f975208982349f61187952f9917ed4508cebffaa2a78abec7a4e595cac`  
		Last Modified: Sat, 27 Jan 2024 01:58:27 GMT  
		Size: 96.9 MB (96869969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca09e400b2901ee2299cbf4c8d7bd0b4673c2725a3478a09ab2ebe6d5a089748`  
		Last Modified: Sat, 27 Jan 2024 01:58:25 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8ba59ce8e3684b523e3099cc589bbb1bfcec89a31fc3cbcc00729b41e5bf5a`  
		Last Modified: Sat, 27 Jan 2024 01:58:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934fd4efc7a4ed1e90d8189e5ef270f54852ef65d9fe0b258e43f30d6258837f`  
		Last Modified: Sat, 27 Jan 2024 01:58:25 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8018686dee71f60782c9b9a1da72c08741df4772076b5b8867565b3811760533`  
		Last Modified: Sat, 27 Jan 2024 01:58:26 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4478a79bf2643959e225b9630c906b05003196146739a3d3eab0d79ea33c1a8e`  
		Last Modified: Sat, 27 Jan 2024 01:58:26 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:cc8dc6bce7dfa8a2c5ab668aeb343b9697cfe85c0371f98b1282953885541435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.1 KB (845096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda31a70255a1fde5c613a4cf815a03872e497ba161b5ec99712a951f581b449`

```dockerfile
```

-	Layers:
	-	`sha256:aa3d7c4ce9922666f5173f219d6fa11ff4752e4d367ed3338c3e3f2180c2ed6c`  
		Last Modified: Sat, 27 Jan 2024 01:58:25 GMT  
		Size: 807.3 KB (807292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10adf305f9ecddc9e11f726271cdb7c22e0a43eba440363fb67d86ebe55d0a71`  
		Last Modified: Sat, 27 Jan 2024 01:58:25 GMT  
		Size: 37.8 KB (37804 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:f4d6cd846ff5e709fb7a0a6255006b6b9dd4509177f51b8638e890b8aca265f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99432603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88026a325d949fb2f4458980f347124840ae1f270655a0999d65e5334efa334`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 22 Dec 2023 00:27:15 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=15
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=15.5
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=8f53aa95d78eb8e82536ea46b68187793b42bba3b4f65aa342f540b23c9b10a6
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 Dec 2023 00:27:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
STOPSIGNAL SIGINT
# Fri, 22 Dec 2023 00:27:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2095ef6b4fb4fda18e7742c1ae925254b33c6a16e337ac453301de35138c9807`  
		Last Modified: Sat, 27 Jan 2024 10:14:06 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf89a242212848a6e54b111c1643243666bfac60a2cbca3b3fb15c09c6fcff78`  
		Last Modified: Sat, 27 Jan 2024 10:14:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea233b71123276a05c3dce8c2a5704c324a5ff2d44cdce2aad62de388ce016f`  
		Last Modified: Sat, 27 Jan 2024 10:20:35 GMT  
		Size: 96.1 MB (96057523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ab22060d58b9821f26311002379e81e68bf19a50e7425832c11770e6889346`  
		Last Modified: Sat, 27 Jan 2024 10:20:32 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a792784f4687c8c2be693f7275b1f058dd02da52c79ec663cf8093b8451522`  
		Last Modified: Sat, 27 Jan 2024 10:20:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4dd18265bfd96470dc414b77cd043297c3bef25e450d28d2dc111f21cbc28ac`  
		Last Modified: Sat, 27 Jan 2024 10:20:32 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c590bde0de5fe19d9f2b3a439c70f95fc4d998c7ed4c2a166553835d1893af96`  
		Last Modified: Sat, 27 Jan 2024 10:20:33 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e389e6b325db7a9270e503c5f7a4159bb1f4a8bd3895959c12b07299fdbab8`  
		Last Modified: Sat, 27 Jan 2024 10:20:33 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:6ebe25295474dc36bc5d346c30ae1bfd6b0ceb9914539b0f5b2405ac3e55a669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.0 KB (842029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb807a9b9c37b8bf9965027bb09323635e518e97512979b6a3df5609d04ef61`

```dockerfile
```

-	Layers:
	-	`sha256:67de19bd62d5ef06b6176d5add0c08153722270267e5f54ce93cf07dd88093e7`  
		Last Modified: Sat, 27 Jan 2024 10:20:32 GMT  
		Size: 804.3 KB (804300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b3e6f6f4b3bf63153703d8f9369f4dfbea7d99c9fcfdfe5bbbe913a62c81ee4`  
		Last Modified: Sat, 27 Jan 2024 10:20:32 GMT  
		Size: 37.7 KB (37729 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:573119ad8c7bf81b6ce6d6742005596f850111a0e7b9c548f80cf155b22fad6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103732944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a700257c5e4ca70fab6382706590f4aa5249604d23e33a5e13c69bd546f09528`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=15
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=15.5
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=8f53aa95d78eb8e82536ea46b68187793b42bba3b4f65aa342f540b23c9b10a6
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 Dec 2023 00:27:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
STOPSIGNAL SIGINT
# Fri, 22 Dec 2023 00:27:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98867b7d9ef52d8ea690ad6ab7a1162c3ffb223f498cfe46c5a0c19b26b5df4a`  
		Last Modified: Sat, 09 Dec 2023 02:05:53 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca1d0e320956171da67959a489db8954c94e3093132a48ee544fcaf765d7784`  
		Last Modified: Sat, 09 Dec 2023 02:05:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fe0d0e9797a7cadebcb9f89807585a8c515935583ddf26492f628af7fe8895`  
		Last Modified: Wed, 13 Dec 2023 01:15:57 GMT  
		Size: 100.5 MB (100473881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a4ba2dbde456e7e1b214ec36f688b360e4d1754406d854dc8344aa400cbaf5`  
		Last Modified: Wed, 13 Dec 2023 01:15:55 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318f140a774fb16573a981e18430b2007857436e11283aa23b78cbf8515876de`  
		Last Modified: Wed, 13 Dec 2023 01:15:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1bf82eb4fc3e196e78278e3254263e09fd9d73c5b6e9e8b8d29b412e42078ec`  
		Last Modified: Wed, 13 Dec 2023 01:15:55 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ddbea549bceb18a4e1383180e36638e9204da685889601e3b5272cb114dd9a`  
		Last Modified: Fri, 05 Jan 2024 02:11:29 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ea67763a55e9370d37933b1e063ac8c7d8172403be482f4574c9888aff335`  
		Last Modified: Fri, 05 Jan 2024 02:11:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:5edf71f03bf97d2a844b47a8650c64b1d290bea994b107d7331aa85fa2c03bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.4 KB (843360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd70ff88d3af51842b58eec27dab916277ed622697cadc37dea0954f2996c42`

```dockerfile
```

-	Layers:
	-	`sha256:e7e465ed3d4e1d5d339f8a454544f9566099e363cba1429ba611a70a17150e2a`  
		Last Modified: Fri, 05 Jan 2024 02:11:28 GMT  
		Size: 805.7 KB (805675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4575dc856dbbfe1bded48b6e02b5de1332a629ecad5eff8fe925b780332705bf`  
		Last Modified: Fri, 05 Jan 2024 02:11:29 GMT  
		Size: 37.7 KB (37685 bytes)  
		MIME: application/vnd.in-toto+json
