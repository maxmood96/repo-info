## `postgres:alpine3.18`

```console
$ docker pull postgres@sha256:99aee0e9ad96a3d7bb7e6f94ff3c04d8459ea651efb58bd626203c1d9bf7a168
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

### `postgres:alpine3.18` - linux; amd64

```console
$ docker pull postgres@sha256:c9ffbd1e51e0695177e1065f25cd37e1420df26130b7f7aa397192acba7c2960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94273688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ddae900cc768101da41b29ef230c71f27dc1b1d064c9925323f4673b0e0adc`
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
	-	`sha256:923f583d82c3500f9693c3a3eecf3199c5483f9971e32152d1ab970568d1f3b6`  
		Last Modified: Sat, 16 Mar 2024 00:00:16 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a118cf760930147354c21e8ceede80385cd0c94feeb6603085ef46755dc4b8`  
		Last Modified: Sat, 16 Mar 2024 00:00:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc16082a9e9277023e241702fd32f406f40098d668243947c80db616494e868`  
		Last Modified: Sat, 16 Mar 2024 00:00:18 GMT  
		Size: 90.9 MB (90854296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2213790a8f6b2788956fbabf524ffb9ba48dcc3fd6d5d35f3fb257213f2223`  
		Last Modified: Sat, 16 Mar 2024 00:00:17 GMT  
		Size: 9.6 KB (9565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef59a207a9d26b16691578cd8686cefdc9e9ea63f3f44bd68a389914c81a405`  
		Last Modified: Sat, 16 Mar 2024 00:00:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8dfeba1f2bab5077ef706d62c874f7d32f0bd796f5fc70188698a425c02ee72`  
		Last Modified: Sat, 16 Mar 2024 00:00:17 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2714b613efdf4807fcba1c633e242ce7edd7b5ba21e0f1901a723684a08dab`  
		Last Modified: Sat, 16 Mar 2024 00:00:18 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ec292f927c62bb1e80b4dc870d436ddcb0de740fe24323a4cd27919ecee7fe`  
		Last Modified: Sat, 16 Mar 2024 00:00:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:dcd6b7748025ae452f1ef259d074c80c4b6bbe602349fb4a3635ecded09786f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.8 KB (993829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7059c9ecc2cab65dad79d125e0d11b242661d489a30e06e90a0407bb40e90dfd`

```dockerfile
```

-	Layers:
	-	`sha256:9933ca0f03be2a97e6a22f56f212018328f226c2d07af13bb5210020d1ba3afc`  
		Last Modified: Sat, 16 Mar 2024 00:00:16 GMT  
		Size: 956.4 KB (956378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79201e05a141724a2c1f4edb9983418b98eb3018164a4cacde7ead1e640f3dc1`  
		Last Modified: Sat, 16 Mar 2024 00:00:17 GMT  
		Size: 37.5 KB (37451 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.18` - linux; arm variant v6

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

### `postgres:alpine3.18` - unknown; unknown

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

### `postgres:alpine3.18` - linux; arm variant v7

```console
$ docker pull postgres@sha256:c280d9f47078f574a3359703f0b9f40bb74d1778c054abc70aecbae67b307455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87552074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f613662af07ddc2400932c9926c88d3a7f2006ea5a7e5b6c8e94da66cd990a`
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
	-	`sha256:dfd951a98e9bc26ad55202a730fbf176a99a4f1dafeac246adac9b93116e6841`  
		Last Modified: Sat, 16 Mar 2024 16:26:55 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83b4bffee9860001c77fb26ccc9519a32dcc2324e1b6490008d4eee80c0ab7a`  
		Last Modified: Sat, 16 Mar 2024 16:26:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbea2b01e42fdf69dfb01fea28640ad7a01b28bcb3f9ac305bf8bfe74a08323`  
		Last Modified: Sat, 16 Mar 2024 16:26:58 GMT  
		Size: 84.6 MB (84633837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97c10628cc43b03a0dea3284748e508dbec03a59cae4024172f58c5d7190d87`  
		Last Modified: Sat, 16 Mar 2024 16:26:55 GMT  
		Size: 9.6 KB (9566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e320ff5ca852f5df9c6ca7c04ff395d01881525ba0b15fc6acf98cf805fb1a7`  
		Last Modified: Sat, 16 Mar 2024 16:26:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe420607d0ddcc8abec391e58c4919c576011d41ded51123940ea7a6cdcc6b8`  
		Last Modified: Sat, 16 Mar 2024 16:26:56 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb5b4602008bcfb7ec54a207fe9461dc4672464351aea80ab224793c808d890`  
		Last Modified: Sat, 16 Mar 2024 16:26:56 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dd8f5e35e7dd26a7809fc1e1369ecb4082627e5051d66d1b24500e882ece35`  
		Last Modified: Sat, 16 Mar 2024 16:26:57 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:04298e6ad8a516e662867084508ce440ab5ae746fef55cc0eeb24e41c8e28bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.8 KB (993829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1914b9ac557413057c8dd931cbc3c4a9175941697814f7184ba1aa6c18b618f`

```dockerfile
```

-	Layers:
	-	`sha256:c08a1ed837b33c37d62a07e66fcf7faa021dde73cab63f59b1afcef1c8b91f9e`  
		Last Modified: Sat, 16 Mar 2024 16:26:55 GMT  
		Size: 956.4 KB (956406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e632b7b5cd4078506a113fa5800fa9c1704215767b129fa2d07de69a6f5fec6b`  
		Last Modified: Sat, 16 Mar 2024 16:26:55 GMT  
		Size: 37.4 KB (37423 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:6eb839decc4ba2136d76516b8d030a5359775ae10d3ec025a92052e12f9f0d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93202819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c11d577318356cdee9bd4cd2fce1ff1d6e86e29e1ba0aaa112caf3811dd871`
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
	-	`sha256:9f0d67f8ee92283d3a70b55534935f9cf573a96846e14b450142f2ee97b0abd7`  
		Last Modified: Sat, 16 Mar 2024 16:13:31 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c4fb2be86da82b8c1a950f073ffb3f9c21075f9798fff81fd347e8cfa19b84`  
		Last Modified: Sat, 16 Mar 2024 16:13:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9ad8773d38449189500ea6296d0fda4e7894787687a39956c275cf96a0f437`  
		Last Modified: Sat, 16 Mar 2024 16:13:34 GMT  
		Size: 89.9 MB (89852611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216b87d45de248927f6485f37fa29802d2404eea38776c9de1e4862c682596b1`  
		Last Modified: Sat, 16 Mar 2024 16:13:31 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b58d956318ef324fe64b45d25361e66f127222aa3a9c4ed8c15be0da497d3a1`  
		Last Modified: Sat, 16 Mar 2024 16:13:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48ac4b9433f0b0eb92fd9e0e504fc5e6b99ef789b5d4f6cc5a6c0d45b7d5d07`  
		Last Modified: Sat, 16 Mar 2024 16:13:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b085a27bbf79d7166cad19af105a460f59f4c5c99b180e38d32f57d4a08d7d`  
		Last Modified: Sat, 16 Mar 2024 16:13:32 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7ea099add77e1e96a1e24595d10608a40b3c638441b48a6a8659ac605191a4`  
		Last Modified: Sat, 16 Mar 2024 16:13:34 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:8f71ed0536a0a2bef2021bcae05584d85fabe61880688c57d1523f69ace2b3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.7 KB (993680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3405954a855708f7e924733a18b90742d41d83ca63e5019ab640ef22b3cc49d6`

```dockerfile
```

-	Layers:
	-	`sha256:a2ea23032034130dde43121fc20a188488c099ce23389077aae36eefce539401`  
		Last Modified: Sat, 16 Mar 2024 16:13:31 GMT  
		Size: 956.4 KB (956387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d89eac6435ee2c9abf32f22b98c03bd6d7a815f608f0a092ab2522abf0b81633`  
		Last Modified: Sat, 16 Mar 2024 16:13:31 GMT  
		Size: 37.3 KB (37293 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.18` - linux; 386

```console
$ docker pull postgres@sha256:7ca4135ac2b19aa4915ed202c80eed4ab0d616425e18941686467d1eaea0a8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99234543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c966fa5e211540a127115b007bb294a4b1373c067d0ced043d93698c5085ead4`
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
	-	`sha256:2c75b04300e553510de820dc0d537c0691bff69605f6ad95587ac56b7791863c`  
		Last Modified: Sat, 16 Mar 2024 00:00:43 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48367c8c74468b7f471455bd65ef939fe8e6430cab2a6d69222b6744b3693b1`  
		Last Modified: Sat, 16 Mar 2024 00:00:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a917b21d71d97aea42aeb2fda0ccf32e6c71b1852fb74981402f1928f1de729`  
		Last Modified: Sat, 16 Mar 2024 00:01:06 GMT  
		Size: 96.0 MB (95978632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e79b3bc8469fbc7a6a3ac8a58685b6b2bb260f1e7da74c4d04cb138878b4bc`  
		Last Modified: Sat, 16 Mar 2024 00:01:04 GMT  
		Size: 9.6 KB (9563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96145211b161107c64abb20abf9b63138c8cf317b77199e3d413b131762a48de`  
		Last Modified: Sat, 16 Mar 2024 00:01:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b403152e11efe8d4777eb2f79d218230651bfc853084ba65a9d7cd51948411`  
		Last Modified: Sat, 16 Mar 2024 00:01:04 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d0de4caa626e37c52aad3eff17b01d9819dc5c74cdadf8857f50abd2b610b5`  
		Last Modified: Sat, 16 Mar 2024 00:01:05 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b414a995607dbb21b846d73964f4b3b9e6c05f1ff78b551aef1edf0bd62f0ba3`  
		Last Modified: Sat, 16 Mar 2024 00:01:05 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:3718dcac8626f84fb1aba58f146444ccc0db09428dd69aeba4dcd74f81e073e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.8 KB (993773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317480683d5636be8125796c35dfaa1d9fba7ec15003da3e42012875da97a902`

```dockerfile
```

-	Layers:
	-	`sha256:250dd89e4e0688438d35c62c03c6a383aebf5a9d5a2e01500d5760040789ca7c`  
		Last Modified: Sat, 16 Mar 2024 00:01:04 GMT  
		Size: 956.4 KB (956358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38b1c6a7b505ec9b3c2626f40ddb8a64ab8a4f0b0debadace4efe98db3880c9f`  
		Last Modified: Sat, 16 Mar 2024 00:01:04 GMT  
		Size: 37.4 KB (37415 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.18` - linux; ppc64le

```console
$ docker pull postgres@sha256:f44cd3e1beb666b70ef8901afa472858669069cab6b1a1a69000871b2cdf1782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (99982747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f2bf0d3e00998bd08db3f9748d6912fed3c8ece03efcc9a38efd07a3f91f78`
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
	-	`sha256:57bf06424f58ac7307d52d4ae986fc96c03d14c3e8c9546673273e53c183a35a`  
		Last Modified: Sat, 16 Mar 2024 10:40:30 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545ceadfd5057505b4e5d6cd51ddf57b0cb73f291f5b2ab2e392c78a73f6318c`  
		Last Modified: Sat, 16 Mar 2024 10:40:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051ead0e67fd07a2bb5cce8bb1f5ca6a48c69219f470fa7b6a4b194ee3342585`  
		Last Modified: Sat, 16 Mar 2024 10:40:34 GMT  
		Size: 96.6 MB (96617411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cee4ba5f50646077df511602812a0f4cd12afbd925f8a3a5934b66944572eb2`  
		Last Modified: Sat, 16 Mar 2024 10:40:31 GMT  
		Size: 9.6 KB (9565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e44918b40191af67c8db8ba994ec0fac7d688cbfa87138a7152a28ece02dac`  
		Last Modified: Sat, 16 Mar 2024 10:40:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ba53ee40eaebf965b7bf02a2b39876eed936e30558a6a598c085fe6d245d19`  
		Last Modified: Sat, 16 Mar 2024 10:40:32 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748b1b890cac94a7397d806760b4a25bfb368dbdc53b34d8d0419eeef43e4680`  
		Last Modified: Sat, 16 Mar 2024 10:40:32 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e239666cc070b08ed64c5f0409e934ed88e08af9e9b1e0934790c2cfedb654`  
		Last Modified: Sat, 16 Mar 2024 10:40:32 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:6b0f01d7cf421fba9497cd2ab4acb8a4865dde6286f047fcd63780c8866d1716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.3 KB (990260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ef572a9094d5cf468e4a5428854d5f71a61b319455cc48b9f75a9190c0989e`

```dockerfile
```

-	Layers:
	-	`sha256:fd9542e2406ba9ce93c4303c97d748021f8f6973594e559d80c0125f13c6dd5d`  
		Last Modified: Sat, 16 Mar 2024 10:40:31 GMT  
		Size: 952.9 KB (952931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9987eba075816d318aabfbdd75a30d5357c085c5eace12a5871b5f1bae7cd27`  
		Last Modified: Sat, 16 Mar 2024 10:40:30 GMT  
		Size: 37.3 KB (37329 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.18` - linux; s390x

```console
$ docker pull postgres@sha256:8a8bde9f370a03a7a0cee59e1e5dc554eac2144bdbc87db2531ca064d83e4a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95933841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e729993e14be65afe264935b417623e3628fd58d42ba487b4148e553cc5db289`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
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
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf260decda6a63ec1e1aad448e571ec50e25aa04f4fe41a8a7c8467fd1d98040`  
		Last Modified: Sat, 16 Mar 2024 10:25:45 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072023fa977b97bad79fe5490620d4365467a2f39216fbc49cdba3aeaffd97b8`  
		Last Modified: Sat, 16 Mar 2024 10:25:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0151474c4de634f46cb6251be7259e4f0875bde1c91af6385a47405f7a550a1c`  
		Last Modified: Sun, 17 Mar 2024 23:46:41 GMT  
		Size: 92.7 MB (92699462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384dbaae23cbac0204e4193b57c4c8c03dec680143c7e820cfece2e807be66f7`  
		Last Modified: Sun, 17 Mar 2024 23:46:39 GMT  
		Size: 9.6 KB (9563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2f9060b53d34ce3e70bee47affd4322e117cb92744024d884aa29ab4d0412f`  
		Last Modified: Sun, 17 Mar 2024 23:46:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2b04777dff331dc595fb14c09c752bc7c1f666a2c48edee929e10db17ba6da`  
		Last Modified: Sun, 17 Mar 2024 23:46:39 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03d438fbd3e12f21bea15bd8f734897f4f82360b38ab58c3822124e2603b669`  
		Last Modified: Sun, 17 Mar 2024 23:46:40 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ebb1f229d071ddd69e54147aee4d82cb978d5909fd6d996821ca3c8bb9adc1`  
		Last Modified: Sun, 17 Mar 2024 23:46:40 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:c63f4140152463bcb2b90289e02233b20f2c8114ead7c7a0bc6d1244cc7271c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **991.7 KB (991708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f268a9ddb4b6884e0da11dea8e3b539216b6fb4f4df1b4964b9dc8456f483d`

```dockerfile
```

-	Layers:
	-	`sha256:671d90a112bfa7b350e1da70271447e2e31d7b746485aa7e00c8bd38cc401a1c`  
		Last Modified: Sun, 17 Mar 2024 23:46:39 GMT  
		Size: 954.4 KB (954424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e43785d17f9add2a12b39a9c09732c9b0acee373b58f4b02a19ef128eb44fb4`  
		Last Modified: Sun, 17 Mar 2024 23:46:39 GMT  
		Size: 37.3 KB (37284 bytes)  
		MIME: application/vnd.in-toto+json
