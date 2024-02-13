## `postgres:16-alpine3.18`

```console
$ docker pull postgres@sha256:67cc5daf4d7e75dcca20514e17371c158998607d87bc70999b3b7dd7cb5b87c1
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

### `postgres:16-alpine3.18` - linux; amd64

```console
$ docker pull postgres@sha256:7301126f8f27879e950feac65f148bb191007d6cd9b9a4a3a949ff85f7adca44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94273624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b569a69e22b6dd3ea2a5b3c9d2a512d956a54100b00e4b6506f3ea41aacb3db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:52:58 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:52:58 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PG_MAJOR=16
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PG_VERSION=16.2
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PG_SHA256=446e88294dbc2c9085ab4b7061a646fa604b4bec03521d5ea671c2e5ad9b2952
# Thu, 08 Feb 2024 19:52:58 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:52:58 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:52:58 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:52:58 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:52:58 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:52:58 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:52:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0c124c11bcb4e5e4a9aa4eeaba655c92c6d5f0f7dc619ef2956fe4b9e2fb81`  
		Last Modified: Mon, 12 Feb 2024 22:00:01 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf293d7cb3a532c4e8b04b6d4f5bc4916743cce9e0e1514eba01556a7064eda`  
		Last Modified: Mon, 12 Feb 2024 22:00:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f39a63ee9938572e746b4ad6aa177d02f2125589375e30e05540ec0c6ce7ef6`  
		Last Modified: Mon, 12 Feb 2024 22:00:05 GMT  
		Size: 90.9 MB (90854238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ae50e5afed4fe7145ee0572edfcb3b93c62e7149ce6b404c54bbe5541dcb37`  
		Last Modified: Mon, 12 Feb 2024 22:00:01 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc937dc6678f83886a76aabc8387e791eee7c5b2c05a806ae442a0281a486a9e`  
		Last Modified: Mon, 12 Feb 2024 22:00:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1717c9c0ad69a9bc0ddbdd0e9261ac2f225f6e7d44015a17be1907e534dc0b`  
		Last Modified: Mon, 12 Feb 2024 22:00:02 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fad5e0d61b735e84de64eec98a2741f64026f15e2f360894e0801f1c12d9f5`  
		Last Modified: Mon, 12 Feb 2024 22:00:02 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac280947fad311ddbfe81236408602f0bb9f35f16fb74d53f5af765fe9f8d66c`  
		Last Modified: Mon, 12 Feb 2024 22:00:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:b94fd2a976ec5f40676332ae0a7e5b4a3c28f927ef3b040794a8c36a0f790f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.9 KB (843945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351c634d73da6d5c83de9f08f2433e3bf02597d93401a02d64319ee6c3963b60`

```dockerfile
```

-	Layers:
	-	`sha256:b13baf2d109c4b4c1a72d55cd8018bc31d6a35dc3113f1ead888b0ef23256e3d`  
		Last Modified: Mon, 12 Feb 2024 22:00:01 GMT  
		Size: 806.5 KB (806494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:595d876ea3ff0fd2b2cb65b970fe9d7b4f39386ecf25e2ff61a47921214c2874`  
		Last Modified: Mon, 12 Feb 2024 22:00:01 GMT  
		Size: 37.5 KB (37451 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.18` - linux; arm variant v6

```console
$ docker pull postgres@sha256:59a4f5c90cf0f372afa3b896703d48560bc4d957b730d7e3a2c10b563d5b6c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92895873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69efac307b8993f665ef90c47420f4f405dfea3fb60007dfbeae840b8b461133`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:52:58 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:52:58 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PG_MAJOR=16
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PG_VERSION=16.2
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PG_SHA256=446e88294dbc2c9085ab4b7061a646fa604b4bec03521d5ea671c2e5ad9b2952
# Thu, 08 Feb 2024 19:52:58 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:52:58 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:52:58 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:52:58 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:52:58 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:52:58 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:52:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f162067667165927cc6eaee841a2797acf104d72473c6b32e22693a0897a64c5`  
		Last Modified: Mon, 12 Feb 2024 22:20:54 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15988adb2b9009a62352560910de674e1e39283cda96101ccf0328d84c0d5855`  
		Last Modified: Mon, 12 Feb 2024 22:20:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed402d940ed8f1368d14f7af4a7a7deebea929c4cc6d214d97391b92e60bfd2e`  
		Last Modified: Mon, 12 Feb 2024 22:20:57 GMT  
		Size: 89.7 MB (89731973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d15fd33988dcd93a58e352ba698c1fd46efc20d73318c7ff0dd5b42e626aaf`  
		Last Modified: Mon, 12 Feb 2024 22:20:54 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be380d6ed25b5188fb3699dc69ed51d936517aa7091f4e4749d70103300c25a`  
		Last Modified: Mon, 12 Feb 2024 22:20:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48e3ee2c5dcc3f263f18a37632fed1d65889a6e5dacac38dce4d08d5dfe3da1`  
		Last Modified: Mon, 12 Feb 2024 22:20:55 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d965264ae52a81261def73ed7c995da5e2ba97da6d59fdaaa9d98a811f6402`  
		Last Modified: Mon, 12 Feb 2024 22:20:55 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb43ffe21a741455f138312c105fedef4d7646b8d7b953e4062a75082ae41bd9`  
		Last Modified: Mon, 12 Feb 2024 22:20:56 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:de1a04b36eaecdf9c485d7dace2a986f8a96be9907fcd4355df81e8ebb0e9f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9423674c7569568f8ad899e0b078fedf909679d5238f1e9f9709bc4bc1a93d24`

```dockerfile
```

-	Layers:
	-	`sha256:dfd9bab29f1b6f32a3f1e34a15bb16df828a27d0416dffb15fa2e2d8909a02ce`  
		Last Modified: Mon, 12 Feb 2024 22:20:54 GMT  
		Size: 37.4 KB (37376 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.18` - linux; arm variant v7

```console
$ docker pull postgres@sha256:b9e041ee1bf1c03e221c2beadd7b8ce944ca7bc8c0ac47e16729a4c45a0e25b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87552110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a6a81adfed28c65e8bdd0d03e6e4c4fe3bac7a55d02122ab12bdd6252187c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:52:58 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:52:58 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PG_MAJOR=16
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PG_VERSION=16.2
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PG_SHA256=446e88294dbc2c9085ab4b7061a646fa604b4bec03521d5ea671c2e5ad9b2952
# Thu, 08 Feb 2024 19:52:58 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:52:58 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:52:58 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:52:58 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:52:58 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:52:58 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:52:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd3b6f1b54990dd494ffb1b65bf336b05d6f789f5529ff89482a0472262b2c3`  
		Last Modified: Tue, 13 Feb 2024 00:17:11 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd7cd37e35818f6d35c46b5ef95dd9a351c4be78e3edaac0624e39f0c4eb42d`  
		Last Modified: Tue, 13 Feb 2024 00:17:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07c4b5fe9583021634a798f572b84a5181816a3ade827918725d0756b528c9c`  
		Last Modified: Tue, 13 Feb 2024 00:17:14 GMT  
		Size: 84.6 MB (84633875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8178ca7f8b6065d66cfa6a0b504d0e27b1d54c4872e2beb9c29a34b8e4ff9a`  
		Last Modified: Tue, 13 Feb 2024 00:17:11 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40519040ea81b712a00668e1e489ee6115379917b8080b33d61f227ebe396425`  
		Last Modified: Tue, 13 Feb 2024 00:17:12 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835d086e04a291f3f9b5def77cb2203c0a8b1da865231bc32a7bb0f9ee5a7ce3`  
		Last Modified: Tue, 13 Feb 2024 00:17:12 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6dc4d747e9c56980400f0cbe8c91149c95df50048fabe1d7819f7c79d6a29fb`  
		Last Modified: Tue, 13 Feb 2024 00:17:12 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac2c445be6869010ddd5189db1be5ff329b8841cdf7612f925793ebf45fad70`  
		Last Modified: Tue, 13 Feb 2024 00:17:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:dc548bebeebe5aaf5b2b2c8a3de5d866510a1aabd8777041b0d9f0c1833f217a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.9 KB (843947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c507339834b82edac8d11039d4dea257f637e71bc060b20d808b4a462de06078`

```dockerfile
```

-	Layers:
	-	`sha256:4dd90ed31b0aee9bb0362031ce4d1ab2a89e3e96c6fb698bfe2f210146b048d0`  
		Last Modified: Tue, 13 Feb 2024 00:17:11 GMT  
		Size: 806.5 KB (806522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b71a8dae3e73d2dd67eadbee786ea2d932190209ab6593c0950857c07ce7d15`  
		Last Modified: Tue, 13 Feb 2024 00:17:11 GMT  
		Size: 37.4 KB (37425 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:c965521314c33f0b43562f35c7c90bd7a5eeed5589e7f0902cf1412a34145cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93203035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f80af476fe51503d2b5612fd37e062d322787684a9092f8152d76a0596efa92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:52:58 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:52:58 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PG_MAJOR=16
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PG_VERSION=16.2
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PG_SHA256=446e88294dbc2c9085ab4b7061a646fa604b4bec03521d5ea671c2e5ad9b2952
# Thu, 08 Feb 2024 19:52:58 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:52:58 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:52:58 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:52:58 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:52:58 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:52:58 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:52:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdffa6c2002e0e6756cd4a14b91c587ee3fa930e296bc42ec44324776923cdd2`  
		Last Modified: Tue, 13 Feb 2024 01:04:09 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fc7af1eb2e43aacadbb162cf37a3e4dba1f130de9c764218a909fe27c2267c`  
		Last Modified: Tue, 13 Feb 2024 01:04:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d97a86e8b38c5c78e96f1592c1996cb9bab226dd470cbc21addd98c7b28f2a2`  
		Last Modified: Tue, 13 Feb 2024 01:04:13 GMT  
		Size: 89.9 MB (89852833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8964e33937e0e3d47fe5ed41670899f1ee5e4d084ef3b31bb3b89fa6e71f83ad`  
		Last Modified: Tue, 13 Feb 2024 01:04:09 GMT  
		Size: 9.6 KB (9562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbd19fda11592a848b6165e50596fdf47987af5c76f62ea2e22011ed0b439d8`  
		Last Modified: Tue, 13 Feb 2024 01:04:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c148bf0c94fa1ab6602feb65a4179066f5cbc537506af254b4bb1cb1dc34ce00`  
		Last Modified: Tue, 13 Feb 2024 01:04:11 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec6e43c248aedc4ac4d084f496701df0a3ff864c91e5203e21da782c613a725`  
		Last Modified: Tue, 13 Feb 2024 01:04:11 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a09d27238a9f95d34d379b5a06029f1ab77d5a844c28019947eab08c9acd2`  
		Last Modified: Tue, 13 Feb 2024 01:04:12 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:4791887f0b51e5bbade522cbdcf84adb07543b2297bb59ef095dc65f131c62b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.8 KB (843796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1576c101ed94595e6027a38cb25a7bf48c8e03eb1df33be416dbed426d31f0`

```dockerfile
```

-	Layers:
	-	`sha256:6bf1ecff4c55a19c6adae1b9a40aab207018c27e774be73f2caddca2e628f37e`  
		Last Modified: Tue, 13 Feb 2024 01:04:09 GMT  
		Size: 806.5 KB (806503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a21f16375adfcb687af2c68d82e091e4e4e03cd06994ca11faaaa9643ce01147`  
		Last Modified: Tue, 13 Feb 2024 01:04:09 GMT  
		Size: 37.3 KB (37293 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.18` - linux; 386

```console
$ docker pull postgres@sha256:64403066c954645a12ab6b686fe1254c95a31d32e259ed1c6830fa073bf68bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99234251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ebe5800a8c4c4bb473677382d36747358661baf12a73864498d76a100a8e86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:52:58 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:52:58 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PG_MAJOR=16
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PG_VERSION=16.2
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PG_SHA256=446e88294dbc2c9085ab4b7061a646fa604b4bec03521d5ea671c2e5ad9b2952
# Thu, 08 Feb 2024 19:52:58 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:52:58 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:52:58 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:52:58 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:52:58 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:52:58 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:52:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94636a4d7adab20b11cc9dc4e51d71a0db224ebe381d77560ae7ebe0b0bf4b03`  
		Last Modified: Mon, 12 Feb 2024 22:00:24 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2f54332fe1532521ae0703d8d1c30a096c6d747d1a60f083a3589d081a7070`  
		Last Modified: Mon, 12 Feb 2024 22:00:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4d02ebef8c22fc760e05104f2599374908f195645a4c08b531aa119d7ad4f3`  
		Last Modified: Mon, 12 Feb 2024 22:00:26 GMT  
		Size: 96.0 MB (95978342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a394da55e5523eb93f3673ba0b1c49ca21e582f777b2408dc78b5653236bd98`  
		Last Modified: Mon, 12 Feb 2024 22:00:24 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d990596cedb7de227bf31a973cac0498352852e40487e09b0ec6fe4b60e1e0`  
		Last Modified: Mon, 12 Feb 2024 22:00:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7292a3e84c9547bcb667dfd0fb29ced904aef0dbd9489a70adb660a79e956652`  
		Last Modified: Mon, 12 Feb 2024 22:00:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04c31ba218b682dbf46e8da7b619b7c29cbb4c2b8ee7d591c8f19cd1d8d07a4`  
		Last Modified: Mon, 12 Feb 2024 22:00:25 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fef7535e21a6439825d10003fc9f0bc63d3f9079e184cdcad85068664bd4dc`  
		Last Modified: Mon, 12 Feb 2024 22:00:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:8e679a20176c6e1d17b160465b9fa53187489660a4da2bc8bae8c37bd25d4149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.9 KB (843889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8a988588b89dd759ffc903f80cb2f7e1f418d7933de3964039b3635ddc3764`

```dockerfile
```

-	Layers:
	-	`sha256:8b22ac1183a3007d04fa3cd54942c0c2aba7470f504ba8b83e2ee560cddd36a5`  
		Last Modified: Mon, 12 Feb 2024 22:00:24 GMT  
		Size: 806.5 KB (806474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:144a1d9ce90b5454878aa98fa16ccd1dd7805f9d1dd301748250fe4595c2d5a2`  
		Last Modified: Mon, 12 Feb 2024 22:00:24 GMT  
		Size: 37.4 KB (37415 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.18` - linux; ppc64le

```console
$ docker pull postgres@sha256:e3c94443ae929c19227b6b9b0d36842b8326f07293ccf4afb3828d30ce99f193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (99982098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31f5fd511219982a50abe47a51d3c735d97cf6c9a4e85355d650766919eb030`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:52:58 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:52:58 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PG_MAJOR=16
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PG_VERSION=16.2
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PG_SHA256=446e88294dbc2c9085ab4b7061a646fa604b4bec03521d5ea671c2e5ad9b2952
# Thu, 08 Feb 2024 19:52:58 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:52:58 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:52:58 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:52:58 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:52:58 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:52:58 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:52:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8902010b016148d7a344a816775bb68a2f2b69cf0eed5857366eb8f807cca9`  
		Last Modified: Mon, 12 Feb 2024 23:27:23 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b51baf31c38d029e4d936e367fa484733715acb0d9b9cd2b169bf5633a341b`  
		Last Modified: Mon, 12 Feb 2024 23:27:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86f83d72d5777dac916bef1fed2ba08f4196f204ba0805c52b0160a2b7b4e55`  
		Last Modified: Mon, 12 Feb 2024 23:27:28 GMT  
		Size: 96.6 MB (96616761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db0f693deef1bd17a4980e2c3564c93c8aa4f344bc806f9e2c57832f71e90c5`  
		Last Modified: Mon, 12 Feb 2024 23:27:24 GMT  
		Size: 9.6 KB (9565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf168e46bca013b87ce1272a3e08c2692f125edb627f62326f52907b10d62fc`  
		Last Modified: Mon, 12 Feb 2024 23:27:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecbe93ede265798df72815f2102c0fc9cad0ed43be981b011f368f9614e110c`  
		Last Modified: Mon, 12 Feb 2024 23:27:25 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae11719a0b2e4c86cd5e404c7a607ba1271353b6c7193219fad56fe64ad3fcf8`  
		Last Modified: Mon, 12 Feb 2024 23:27:25 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3899fd17fe01bf1242f4e01efd2f5b96a934a41536214aecb48725a44df29d`  
		Last Modified: Mon, 12 Feb 2024 23:27:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:d0e7a8bbb9f346b0e2139bf03844eb65e37b6b32bacb0f7c2f96cc2dd9e9866d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28128b8ed8ec41823ae501ce3f4235c8a9c8a380999ea88bd4ce2a2042c72b34`

```dockerfile
```

-	Layers:
	-	`sha256:02f981782d98aa48a7d106a576c24d975e5d705d229ed0680b85597c596c13dd`  
		Last Modified: Mon, 12 Feb 2024 23:27:24 GMT  
		Size: 803.5 KB (803471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82afde75137973697e50fd419fffa0014a5abe45d3532f85127a305030864147`  
		Last Modified: Mon, 12 Feb 2024 23:27:24 GMT  
		Size: 37.3 KB (37329 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.18` - linux; s390x

```console
$ docker pull postgres@sha256:9c28dd95f04fe8199f8ad06aaa26eda715798e8585a4e4f23fe1b455088094bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95919047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ac093a2f95f1c01907d37bacfedb5d706c9c27f86e38bf9171a266d6ec2446`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 22 Dec 2023 00:27:15 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=16
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=16.1
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=ce3c4d85d19b0121fe0d3f8ef1fa601f71989e86f8a66f7dc3ad546dd5564fec
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1232613ee9bc8df1c9014bf62023a3ce795b33a1a50786be93cf2ce57ee9e649`  
		Last Modified: Sun, 28 Jan 2024 11:00:06 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65defa579abc615d44ef993e684c6dbf65d06b59c8bb4f049508e15384da0812`  
		Last Modified: Sun, 28 Jan 2024 11:00:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4750763eb2130ee92569844ad1e68cc73ae12cde6063d0a18e905b6a83b886`  
		Last Modified: Sun, 28 Jan 2024 11:00:07 GMT  
		Size: 92.7 MB (92684665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfcf2d0d4ecec08d5c2575809c311aef30531f1bc7ccb044139fc9555c2a24f6`  
		Last Modified: Sun, 28 Jan 2024 11:00:06 GMT  
		Size: 9.6 KB (9571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be5fa7b2892fe83905f7918542606dbeaf08761bb3211c7819d70f6abdd607c`  
		Last Modified: Sun, 28 Jan 2024 11:00:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100546668e1e8394af30259b0fdce1dfd0f573f07e5a7838c0631b67c28f4b6c`  
		Last Modified: Sun, 28 Jan 2024 11:00:07 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5839d2ab2e629bc652f2ca297f5e668eaef053daf76d867d16d6e41a7e59b7`  
		Last Modified: Sun, 28 Jan 2024 11:00:07 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2da6a502e965e8a50ad6eefac6bb387d98c3d6b48c06e67cac963c81d7d12f5`  
		Last Modified: Sun, 28 Jan 2024 11:00:07 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:442516e35a3e38f305cd7f3445051147fc0dd562583bef5262c647613cea16c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.1 KB (842143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55be9a83b8f9c3ad546b655554637999d7ebb3356a03bfb621c04ec3c6e777d`

```dockerfile
```

-	Layers:
	-	`sha256:475aefc165b0dab1f86b8f39aba74679141a551c813eeb3892fde2aeec721717`  
		Last Modified: Sun, 28 Jan 2024 11:00:06 GMT  
		Size: 804.9 KB (804858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00afd2c02b2c18cde0ab5c75d9c49f030c462069d8f2bc00ab86549845260cfb`  
		Last Modified: Sun, 28 Jan 2024 11:00:05 GMT  
		Size: 37.3 KB (37285 bytes)  
		MIME: application/vnd.in-toto+json
