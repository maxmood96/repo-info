## `postgres:alpine3.24`

```console
$ docker pull postgres@sha256:1b1689b20d16a014a3d195653381cf2caa75a41a92d93b255a9d6ea29fd353aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:alpine3.24` - linux; amd64

```console
$ docker pull postgres@sha256:3f0182f7f06d949972a1d1901ff774e6d0b7c03ca95a27a12958d713fe5ea153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119956920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d320a6265d9f49e7166e21518b664b9291dc203b9d63416c5875c8e3db7150`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:57:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:57:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:57:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:57:50 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:57:50 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:57:50 GMT
ENV PG_MAJOR=18
# Tue, 16 Jun 2026 22:57:50 GMT
ENV PG_VERSION=18.4
# Tue, 16 Jun 2026 22:57:50 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Tue, 16 Jun 2026 22:57:50 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:10 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:10 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:10 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:10 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 16 Jun 2026 23:00:10 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:00:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:10 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:10 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:10 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fea78c5766f799a8a4075ccb49814f9c4f5fa90653c02eaa31bd6b5ea458072`  
		Last Modified: Tue, 16 Jun 2026 23:00:26 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5547cc751f26e02ff946bc11210adbe20f6444392485b197f937b176e680ded8`  
		Last Modified: Tue, 16 Jun 2026 23:00:27 GMT  
		Size: 900.3 KB (900254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b08d7cbdb42c3661cff0b29d4d35f2f6c7435d20d9705f17ad8725fde46556a`  
		Last Modified: Tue, 16 Jun 2026 23:00:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21111c9f880cbf02b71a8a59ee3b437a513dbca2963e281f787afd1b799e64fb`  
		Last Modified: Tue, 16 Jun 2026 23:00:30 GMT  
		Size: 115.2 MB (115183857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f29473cdb7bb88733afb496a8db6292c82d2a764158bc5650553d7f4adaaa8`  
		Last Modified: Tue, 16 Jun 2026 23:00:28 GMT  
		Size: 18.9 KB (18920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60689792c913e9e339ec8976b4ea711f9b25680542f816718b030277c6e5f57`  
		Last Modified: Tue, 16 Jun 2026 23:00:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e22369980478b8a9a88f7ba2bcfb9bcfdb9ab99e8177a257c765ee65516a63a`  
		Last Modified: Tue, 16 Jun 2026 23:00:29 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5129de87fb5a2d4bbd82f69a00ef47257eb377e9dd99983e8e0ed590bfb0917`  
		Last Modified: Tue, 16 Jun 2026 23:00:36 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:72a83284df4e9f8cfe5dd7a14e8856f12f938a224d623c2149f74124183c6c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.3 KB (658306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392d596a74d651dbc4ccde618c65f2fe409661647c69b473254879aa02af674f`

```dockerfile
```

-	Layers:
	-	`sha256:dde5f6f78040a6291283776e1f784c92c5925ac144a208081a8993b11f42ca8d`  
		Last Modified: Tue, 16 Jun 2026 23:00:26 GMT  
		Size: 617.3 KB (617258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9456889e1bdb6c9c81544483bf30219f558802782f7856f4e2625b4afa7d389`  
		Last Modified: Tue, 16 Jun 2026 23:00:26 GMT  
		Size: 41.0 KB (41048 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.24` - linux; arm variant v6

```console
$ docker pull postgres@sha256:8e1e6f2fdcf19f268f9fac3a4fdef66db53f999506f9f87f56e2ff485e65a8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116130116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2850f881b2b0ce767130bbb8336195c0ba569137ee6be883f2e489ed8622516`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:58:29 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:58:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:58:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:58:33 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:58:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:58:33 GMT
ENV PG_MAJOR=18
# Tue, 16 Jun 2026 22:58:33 GMT
ENV PG_VERSION=18.4
# Tue, 16 Jun 2026 22:58:33 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Tue, 16 Jun 2026 22:58:33 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:01:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:01:38 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:01:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:01:38 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 16 Jun 2026 23:01:38 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:01:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:01:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:01:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:01:38 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:01:38 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:01:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad605862ed81017e717427c35aa466359f4f9067b90d4fe15b532ef49793e865`  
		Last Modified: Tue, 16 Jun 2026 23:01:52 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a0b9e23752320ff5df4c3d9da8ec2d3a9f54e1de02153863517be27550c82f`  
		Last Modified: Tue, 16 Jun 2026 23:01:52 GMT  
		Size: 864.6 KB (864624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3780a74ccd62a307908bf2fff2478c755a5cd4381c6be1546b1be83f45749972`  
		Last Modified: Tue, 16 Jun 2026 23:01:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2cc390937979cdd1f66ce788e46b37cabee48226c812c65cbe94c541700a5e`  
		Last Modified: Tue, 16 Jun 2026 23:01:55 GMT  
		Size: 111.7 MB (111685628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6400d59a6bbe93fd5879a78e41b0aa14fa83abe63b9865eb6ec7dcef16c391f`  
		Last Modified: Tue, 16 Jun 2026 23:01:53 GMT  
		Size: 18.9 KB (18921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6412c9b5b72726c154c4a5c397e09b89832db988cfdccb53f08031fee7d66c44`  
		Last Modified: Tue, 16 Jun 2026 23:01:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ab06b48987af1d17e7af8df873d2376d90680cb9c4c04b7d038ccf113d13a0`  
		Last Modified: Tue, 16 Jun 2026 23:01:53 GMT  
		Size: 6.1 KB (6094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9d9662f80f502a34da2308b92bd781acd0556e234f7b61284d80e4d962e11c`  
		Last Modified: Tue, 16 Jun 2026 23:01:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:ff724e09e2ff98af785685f0e8653b5ac08c5928250f4b4f998cdda097ee5d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 KB (41006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7fc01970bca64c672993666f4933b20c093554350797005433ab532c1acaed`

```dockerfile
```

-	Layers:
	-	`sha256:fa7b982130426854d872620f7826e7ed0d877f3c3aab6037f361e178fd77fd85`  
		Last Modified: Tue, 16 Jun 2026 23:01:52 GMT  
		Size: 41.0 KB (41006 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.24` - linux; arm variant v7

```console
$ docker pull postgres@sha256:716d217a866b2cae8e4e9f81eaceb6fd9ab344970e5114a20b50617c301c0093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.7 MB (109706275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec68b857fb5edb2ca61767071f0b063eba25ff423f3300e07324d96f4adc2f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:57:36 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:57:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:57:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:57:40 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:57:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:57:40 GMT
ENV PG_MAJOR=18
# Tue, 16 Jun 2026 22:57:40 GMT
ENV PG_VERSION=18.4
# Tue, 16 Jun 2026 22:57:40 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Tue, 16 Jun 2026 22:57:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:30 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 16 Jun 2026 23:00:30 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:00:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:30 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:30 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d30475b80f928512747a8ce9adc0b4ad9229130244f3b258cd34083ab8ec30`  
		Last Modified: Tue, 16 Jun 2026 23:00:44 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e94f569ab76e4c75076374599f74e1340c0d3b9601ae8beace7d3fd05558750`  
		Last Modified: Tue, 16 Jun 2026 23:00:45 GMT  
		Size: 864.6 KB (864634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3fe0bec7d4c928caee1bc99ab675f734bbdc06e6483ef527ee6ea3543a0b60`  
		Last Modified: Tue, 16 Jun 2026 23:00:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940c286de3ea0962749b4d682ee836baa1675f49976b0dac1bbe1aefe37a1de6`  
		Last Modified: Tue, 16 Jun 2026 23:00:51 GMT  
		Size: 105.6 MB (105554609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eff221cd9cdf2496153904d1b8da1aaa9e6a67f31149a3bd6a044e582fe1fa6`  
		Last Modified: Tue, 16 Jun 2026 23:00:46 GMT  
		Size: 18.9 KB (18920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d78aa8cef68f48ed99ccf451d43265e4364a53cdcc78285551508e30486d382`  
		Last Modified: Tue, 16 Jun 2026 23:00:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df280c4b2a0c67499bf56b88df79a9290524abf443e34e0454c43ae83cf7a23a`  
		Last Modified: Tue, 16 Jun 2026 23:00:47 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3b9c195a5dfa952debe45920b1b259ffc29dc8c48d2f5483dd27b26b834d1d`  
		Last Modified: Tue, 16 Jun 2026 23:00:48 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:8e46dd97ba01a6c40083c34a3664deaf175c9f4a460da80b9cc118e20695c39d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.9 KB (657882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918c36975c3f1b8fdc3d74bff3ef4461dec7285e043ace7f3b499b4184b95b06`

```dockerfile
```

-	Layers:
	-	`sha256:cf5a20838849c9ad2a3cf218bdfc2f439cce7788286827154ea28a415d215fe2`  
		Last Modified: Tue, 16 Jun 2026 23:00:45 GMT  
		Size: 616.7 KB (616660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e9a4e40d421dfb47a62a223a1c0c7a3df9175cc00fc74cdde33fd05d0aabed0`  
		Last Modified: Tue, 16 Jun 2026 23:00:44 GMT  
		Size: 41.2 KB (41222 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.24` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:7e291ba5fc56f2012e6194cd9283de8eea3d0e86b945a375586e8c9fd698ecb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117787526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196c14af9198cb978cdb6be4ea475ae983e6197093c52172fe36b6476fc8fad9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:57:38 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:57:41 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:57:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:57:41 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:57:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:57:41 GMT
ENV PG_MAJOR=18
# Tue, 16 Jun 2026 22:57:41 GMT
ENV PG_VERSION=18.4
# Tue, 16 Jun 2026 22:57:41 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Tue, 16 Jun 2026 22:57:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:04 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:04 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:04 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 16 Jun 2026 23:00:04 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:00:04 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:04 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:04 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:04 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:04 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e013ed837df7fe4c6ae8c9d2aba9db78a6619fd666a6a8b0e2cfabd88d5f85`  
		Last Modified: Tue, 16 Jun 2026 23:00:21 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c934735f2d6fb8d528eae504928a6b442d40a314b5b5630ff9effeeddf3c2a0`  
		Last Modified: Tue, 16 Jun 2026 23:00:21 GMT  
		Size: 852.3 KB (852270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebd74850c876d29c9d1f560ec4c1bfb52e1df6ea7fcc9370d6cfc8c2254a2cd`  
		Last Modified: Tue, 16 Jun 2026 23:00:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9502c1ae2e03ce2e7506a486dcaa13cf5013df8ee05d567df9b2bf06e159fa77`  
		Last Modified: Tue, 16 Jun 2026 23:00:24 GMT  
		Size: 112.7 MB (112725802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99868dd8ab498878e4a2d33a4a28c98c245c68a8f10c55da760c5e4cbdba996`  
		Last Modified: Tue, 16 Jun 2026 23:00:23 GMT  
		Size: 18.9 KB (18920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ed40f595e1f51b4ef776c2b77e4339724ba23b3973ad31cbfc5edc715be465`  
		Last Modified: Tue, 16 Jun 2026 23:00:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc686db35da57168c619fa618cb55c80ed0425a5b5fb2a2d80c3a22d73986d5`  
		Last Modified: Tue, 16 Jun 2026 23:00:23 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc703c5f85e3aad0a469eee3b59bdfa403d72b4b0752af4f15431b96beea5590`  
		Last Modified: Tue, 16 Jun 2026 23:00:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:f82d43ece9039d0987023ab99d75ad0abb05d44b7e02c604a71521f8379ca6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.0 KB (657954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3acb39782d79bb0418b57c5614d0c5561bc25fdc0f8ec80602a6005e0e13e7c2`

```dockerfile
```

-	Layers:
	-	`sha256:6a391b63458b9f228f3d126c37c3bdbcfc8ba633f6bea30843685a9f0e18a622`  
		Last Modified: Tue, 16 Jun 2026 23:00:21 GMT  
		Size: 616.7 KB (616688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e6770e9240d4bdf3aab7256481f9c169543878d2a1536e7aeaf8d710014cb81`  
		Last Modified: Tue, 16 Jun 2026 23:00:21 GMT  
		Size: 41.3 KB (41266 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.24` - linux; 386

```console
$ docker pull postgres@sha256:72f702819bc91cac2265cbe78e4c3ef4c45694f83d63a6829657581accd038e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126758260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9085577288b7960aabdfede4052e0ce1694f5983fdc523e9ea760b5bece1f205`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:57:58 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:58:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:58:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:58:01 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:58:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:58:02 GMT
ENV PG_MAJOR=18
# Tue, 16 Jun 2026 22:58:02 GMT
ENV PG_VERSION=18.4
# Tue, 16 Jun 2026 22:58:02 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Tue, 16 Jun 2026 22:58:02 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:31 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:31 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:31 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 16 Jun 2026 23:00:31 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:00:31 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:31 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:31 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:31 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfd5ed214997056d321b613003bd22e09a77a8ad36825a0babceaf896984af8`  
		Last Modified: Tue, 16 Jun 2026 23:00:49 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bbe12c92f0b501a4feebcdbd60e2fe37b1dc7541878a886b497e8c43d6b03c`  
		Last Modified: Tue, 16 Jun 2026 23:00:48 GMT  
		Size: 868.4 KB (868441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248a64a1f5790f4c876b0a63ce2bd0e70f05f12ed182b592a4a43411c54d65c1`  
		Last Modified: Tue, 16 Jun 2026 23:00:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef335d692c04a665c0826907997c791052e8a4a76d9f4231de73a5adf5030162`  
		Last Modified: Tue, 16 Jun 2026 23:00:53 GMT  
		Size: 122.2 MB (122193263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4906c9bd39be8d15e37138b6ae5e1a45319badf5ecfb31bddbddeb971ebfde71`  
		Last Modified: Tue, 16 Jun 2026 23:00:52 GMT  
		Size: 18.9 KB (18920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d630638447ffa104763b21d6db8ca996cb1b3d4dbb46894b123627aae7a8d2ca`  
		Last Modified: Tue, 16 Jun 2026 23:00:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a27999e8c60b56e259ce8b4cefedeb5207167c66655acbac267f731bb3a16ce`  
		Last Modified: Tue, 16 Jun 2026 23:00:52 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64fe14184b8d1ab3352de6f3dc6693d8cb48c1272d0bf1787b0ce93222d7ceb`  
		Last Modified: Tue, 16 Jun 2026 23:00:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:4d25e6196da3a06ec0b55822295b3d8a7e5a803eb3fd97b4d0c484920b630595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.2 KB (658217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e33f7c5482175db676f635896c8245d46e19efcd27c1b9a9eb209f62094fb5`

```dockerfile
```

-	Layers:
	-	`sha256:d2c1e1f2c94a906fc3494b160ee775527ae8cdd76f13c1c069771abad4985ded`  
		Last Modified: Tue, 16 Jun 2026 23:00:47 GMT  
		Size: 617.2 KB (617223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a712b2db5daef2b822af0365722af1223e15b32909ab70891d35f118960049ab`  
		Last Modified: Tue, 16 Jun 2026 23:00:48 GMT  
		Size: 41.0 KB (40994 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.24` - linux; ppc64le

```console
$ docker pull postgres@sha256:24adcdd19fb2567a8b525e2b741bab3f745790ace696293ca0d01dc3f4ffce51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122935486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea836129591cc4701dccca9079f03e644b85a3462b48f43b019f57aeeda288fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:56:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:56:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:56:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:56:29 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:56:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:56:30 GMT
ENV PG_MAJOR=18
# Tue, 16 Jun 2026 22:56:30 GMT
ENV PG_VERSION=18.4
# Tue, 16 Jun 2026 22:56:30 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Tue, 16 Jun 2026 22:56:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:05:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:05:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:05:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:05:47 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 16 Jun 2026 23:05:47 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:05:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:05:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:05:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:05:48 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:05:48 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:05:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a550c138b135a89330347b3a13776cce136b1e19d05c3e2b10571ce2135769`  
		Last Modified: Tue, 16 Jun 2026 23:01:22 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86fd92e78cd7b0d10ecc0f0da5decbed7534334b833b91ed30473a9d6fcb1f`  
		Last Modified: Tue, 16 Jun 2026 23:01:22 GMT  
		Size: 857.4 KB (857445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f7c2433d0811625666a0f10e6fbc0db707597de61db43eda49dc9457e337f`  
		Last Modified: Tue, 16 Jun 2026 23:01:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670ee415e7ec7277542698ebc2b9998e80f40f31256b2f631778779aa3e0be38`  
		Last Modified: Tue, 16 Jun 2026 23:06:22 GMT  
		Size: 118.2 MB (118238210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b70894bc294c96719488c7e4eaf36ef6acecc34690d3f77e6876efc37fc8e4a`  
		Last Modified: Tue, 16 Jun 2026 23:06:19 GMT  
		Size: 18.9 KB (18928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60669d3d1446474a68db464a6100f19ec993e2fa3e2c8b8e6f1ea093f63fcdc`  
		Last Modified: Tue, 16 Jun 2026 23:06:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca8cd54e526fc906f908dbd2a713d550ef9c05a933b1e32da184cdb7cf5db81`  
		Last Modified: Tue, 16 Jun 2026 23:06:19 GMT  
		Size: 6.1 KB (6102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71849f6c2be7333dffd35d0583e61582d393281a167da8f85fca08d46873a904`  
		Last Modified: Tue, 16 Jun 2026 23:06:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:9ddda8c2db89db8862172c92cc078d2ce326fef85af0cec24daaa71efe3b4bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.1 KB (656107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebbe4f016624b4bab46d49c875f76d7229e89eb4266a36f359d7fa4a93db264`

```dockerfile
```

-	Layers:
	-	`sha256:22b0f82db4eaf66d1ecc130ecd725dcb82151827c563c9624cb25070f6d3b64f`  
		Last Modified: Tue, 16 Jun 2026 23:06:19 GMT  
		Size: 615.0 KB (614991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc094b093627c746d7df281336164969edd2251ac72f53b3c3793076e5f94f10`  
		Last Modified: Tue, 16 Jun 2026 23:06:19 GMT  
		Size: 41.1 KB (41116 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.24` - linux; riscv64

```console
$ docker pull postgres@sha256:1d6d599e5c492c70d611850a0020508ac2a4fe7d17c13a92418084df8b8f8c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122428744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f139c20b0b6c14f9960f6aed70b46b17342e95630915533880e83be4267213`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Wed, 17 Jun 2026 20:22:02 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 17 Jun 2026 20:22:13 GMT
ENV GOSU_VERSION=1.19
# Wed, 17 Jun 2026 20:22:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 17 Jun 2026 20:22:13 GMT
ENV LANG=en_US.utf8
# Wed, 17 Jun 2026 20:22:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 17 Jun 2026 20:22:13 GMT
ENV PG_MAJOR=18
# Wed, 17 Jun 2026 20:22:13 GMT
ENV PG_VERSION=18.4
# Wed, 17 Jun 2026 20:22:13 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Wed, 17 Jun 2026 20:22:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Wed, 17 Jun 2026 23:08:07 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 17 Jun 2026 23:08:07 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 17 Jun 2026 23:08:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 17 Jun 2026 23:08:08 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 17 Jun 2026 23:08:08 GMT
VOLUME [/var/lib/postgresql]
# Wed, 17 Jun 2026 23:08:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 17 Jun 2026 23:08:09 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 17 Jun 2026 23:08:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2026 23:08:09 GMT
STOPSIGNAL SIGINT
# Wed, 17 Jun 2026 23:08:09 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 17 Jun 2026 23:08:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63bc382ee77772838b6762efb5dc9918aac46cc99c959111411a578a706e8e9`  
		Last Modified: Wed, 17 Jun 2026 21:18:05 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac745ca8a6a40fa8931eea62c6eada5afee35c1c91aede732f42ba0aba848664`  
		Last Modified: Wed, 17 Jun 2026 21:18:05 GMT  
		Size: 844.9 KB (844939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37c739103d625ef104f1832bc1629a5055aa3b92c081dbc223595e504ae6f8e`  
		Last Modified: Wed, 17 Jun 2026 21:18:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ef552a78c45569285a3ab5f0b52fd51eeb38475ba5062e972760d39ce11f67`  
		Last Modified: Wed, 17 Jun 2026 23:11:29 GMT  
		Size: 118.0 MB (117983023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f14cae223d7a8adce5d37d6c2243d008d6135fc7a7db28490729691b95c7d23`  
		Last Modified: Wed, 17 Jun 2026 23:11:11 GMT  
		Size: 18.9 KB (18920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b70a1b020513c6c89f792dfb08473630268d68fb09ca1df234280a16f42003d`  
		Last Modified: Wed, 17 Jun 2026 23:11:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d53b6876991f70fef85d97995d382517dee0859bd85de49d3d91e3fbd7fd385`  
		Last Modified: Wed, 17 Jun 2026 23:11:12 GMT  
		Size: 6.1 KB (6103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b762e6f02baa9f948ae0cdd43894f8b1fc36cb28ca37ca1699620bd06111c71`  
		Last Modified: Wed, 17 Jun 2026 23:11:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:b2aea91b8c0efc84819e405d94c01f5f5c5e66d6e00df613ce1da194a79ca131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.8 KB (657765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56907c360887fd840baa32b0648ad45198ac33bc490ae5e32e4a6cee7a07af9e`

```dockerfile
```

-	Layers:
	-	`sha256:2aa2a560aa9fe88b8aace363810b675ada5bd6b07b7fa2e0c8d2328d16ace8c1`  
		Last Modified: Wed, 17 Jun 2026 23:11:12 GMT  
		Size: 616.6 KB (616649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9273e9ed2336bfb3342592d51b52eba2f5a305e92152bacd9a3ea47f69c08a1f`  
		Last Modified: Wed, 17 Jun 2026 23:11:11 GMT  
		Size: 41.1 KB (41116 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.24` - linux; s390x

```console
$ docker pull postgres@sha256:dee264e7de8405ea9b241af68dcc4ace1f533eee6521579ccf3ed2cd46500913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126561609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a4f53299bc564eb509a82862d548d4bc94c652e7d94f944d13ae4c2ae05ae5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:56:31 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:56:34 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:56:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:56:34 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:56:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:56:34 GMT
ENV PG_MAJOR=18
# Tue, 16 Jun 2026 22:56:34 GMT
ENV PG_VERSION=18.4
# Tue, 16 Jun 2026 22:56:34 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Tue, 16 Jun 2026 22:56:34 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:01:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:01:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:01:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:01:17 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 16 Jun 2026 23:01:17 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:01:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:01:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:01:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:01:17 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:01:17 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:01:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52132c4d8fde8082c15540b29256e2360f2c6de68191ad0e46bc71ec74cdc17f`  
		Last Modified: Tue, 16 Jun 2026 23:01:43 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abc6a5451d4cc8391999b7fe99a4a79df7ab9b3d307f2f9e012ae4ea28dfb70`  
		Last Modified: Tue, 16 Jun 2026 23:01:43 GMT  
		Size: 874.5 KB (874490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25afd8b2db677bb30b49528aabcdca1265a11efa62c177e4a6416ad35f153003`  
		Last Modified: Tue, 16 Jun 2026 23:01:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737d7cd4bfd7c3092269ffa23d84e9f259b6557ae444afbfdff4d38d835e819e`  
		Last Modified: Tue, 16 Jun 2026 23:01:46 GMT  
		Size: 122.0 MB (121951389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff9fbba1f5bb5f510d823bb539e230d772ea623fe39297f0a3cb35b1aaf7691`  
		Last Modified: Tue, 16 Jun 2026 23:01:43 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3def601e454f511b20cadd81d461d5328ecf1abdc92501692d927cb1bc1fb18`  
		Last Modified: Tue, 16 Jun 2026 23:01:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3279403ac8e9d6f99ea11bda7ac5cf3f23ea6a95175cb3b355a61ec63d9deacd`  
		Last Modified: Tue, 16 Jun 2026 23:01:44 GMT  
		Size: 6.1 KB (6093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f25a1277c31e4a9cdb0f6e7e02b5fa787c57985fbb0efb024a1a14d80c318c`  
		Last Modified: Tue, 16 Jun 2026 23:01:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:4573225b6a23d0ac2b3d0234718b2c7aa3569530a392977160ff593f2d787d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.7 KB (657655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02944c54abccce960aad78549575c91e8bf82856cbb1657f4532d8d7a91dccd7`

```dockerfile
```

-	Layers:
	-	`sha256:712c6d667d2fe89255206a6012ba04745f23dfafcd0944ada10567e4a6776000`  
		Last Modified: Tue, 16 Jun 2026 23:01:43 GMT  
		Size: 616.6 KB (616607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3defdc0c554547b40724c92ea9b09ff2ad6107beded786bbf2ee0e6ce8aa47a`  
		Last Modified: Tue, 16 Jun 2026 23:01:43 GMT  
		Size: 41.0 KB (41048 bytes)  
		MIME: application/vnd.in-toto+json
