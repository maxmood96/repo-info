## `postgres:16-alpine3.20`

```console
$ docker pull postgres@sha256:52bba373df3c13594014b5e9ccc9f3c2cdb2221d50db1a91ec64570819f18aba
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

### `postgres:16-alpine3.20` - linux; amd64

```console
$ docker pull postgres@sha256:4d41c90ccdf9609ad551f8ef1244333d87a2f6bcfabc8ef90f9cef536423f09c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99208110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d520655e8467285fa28a07c223fa93941dbe1afd03e1a03bb8888e9bb897d7f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:14:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_MAJOR=16
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_VERSION=16.6
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_SHA256=23369cdaccd45270ac5dcc30fa9da205d5be33fa505e1f17a0418d2caeca477b
# Thu, 21 Nov 2024 20:14:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:14:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:14:24 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:14:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:14:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9ff5ead5be1dc54d4b61c93b29420cd122fb7a78fdf25a0a575fe3ee070de2`  
		Last Modified: Fri, 22 Nov 2024 20:27:49 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7795ec6b4e69aa4302ec96f8ed7f3d628c7c2e47b185fca40c641c48e8979a4a`  
		Last Modified: Fri, 22 Nov 2024 20:27:49 GMT  
		Size: 1.1 MB (1119766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b767ae82bd207b3eb1b5f6adb8e4da0985cd2310de0bde47b8142f22c54813db`  
		Last Modified: Fri, 22 Nov 2024 20:27:49 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ca9f1cbb88a0d67d548cbfb037c89e92d7d632b63a1698e0cca17fc9dde2c1`  
		Last Modified: Fri, 22 Nov 2024 20:27:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f573ba0dbe7be5ee587cf396dbb1be0b68114f0163e7ddd1ca62ac5da9c60e91`  
		Last Modified: Fri, 22 Nov 2024 20:27:52 GMT  
		Size: 94.4 MB (94447710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec60fa6141a6b24d7ec9c4b47ac9f7ffebf03053d9bc8ea7a5e71863f4e1c0d4`  
		Last Modified: Fri, 22 Nov 2024 20:27:50 GMT  
		Size: 9.6 KB (9556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aba07e7c88fda68893de29033c2be162f2669ad700c794e150ceea844211ce6`  
		Last Modified: Fri, 22 Nov 2024 20:27:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b4e8d2f73dff59606341c6e6fbb0cd6195b49f9bee8dae5fa6d0b9cf02a439`  
		Last Modified: Fri, 22 Nov 2024 20:27:50 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61746059f1b7cb83207217981088f1bb6edf33d07244ac2e5a55232c9b2e05c`  
		Last Modified: Fri, 22 Nov 2024 20:27:51 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a14dc5a5d260e95ae806ba6abf7204eddda0baa944c3c98a77eb472e8ccc88`  
		Last Modified: Fri, 22 Nov 2024 20:27:51 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:159695a3b4d42b9a6e51c03a45366a9a4ffca83447dcba068fd8833567ee4ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.8 KB (636832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89cb275668bb1ef79c67a862457579bc04df8b244d2a037ffedc3243369a872`

```dockerfile
```

-	Layers:
	-	`sha256:f6bca27f1a8e69478f9af65082d8b1c5151fbb2c30f4c30fe159359421f086ac`  
		Last Modified: Fri, 22 Nov 2024 20:27:50 GMT  
		Size: 591.0 KB (591015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:367bee19f4881c9d206ff98aaaad8d6d22384cb4e0e1a32da9bf6d9562464646`  
		Last Modified: Fri, 22 Nov 2024 20:27:49 GMT  
		Size: 45.8 KB (45817 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:3a3c66890175b7b53970d0377def746cdf08292fd7e2d65ee3f26184817bc00b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97576638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9337ddd1a2bbb0344fcdc46b15f31c2124cb79f0de72809ee1924f5758f354`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:14:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_MAJOR=16
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_VERSION=16.6
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_SHA256=23369cdaccd45270ac5dcc30fa9da205d5be33fa505e1f17a0418d2caeca477b
# Thu, 21 Nov 2024 20:14:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:14:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:14:24 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:14:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:14:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c571936168ff49222fc45202f5453daceaaad85841344e7a56766ac0c06bcc0b`  
		Last Modified: Tue, 12 Nov 2024 05:37:05 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd27d05dad1bb8227f4e72ddcbdcd2601f74b55f8b2929cff613d173bc82672`  
		Last Modified: Tue, 12 Nov 2024 05:37:05 GMT  
		Size: 1.1 MB (1086464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68300102007bc93827d658bcc2e3930a994d78385553143780dadcc3f284915a`  
		Last Modified: Tue, 12 Nov 2024 05:45:35 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef5933ae7af9d77048b5e8ce8dc6807af55c837feaeaecb0fac68b44b61199d`  
		Last Modified: Tue, 12 Nov 2024 05:45:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e23483f87947906cd068594b7048bb7ff64ff46b61a615e20b1da74a1e8f9bb`  
		Last Modified: Fri, 22 Nov 2024 20:36:39 GMT  
		Size: 93.1 MB (93106840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935ca3ed081d4a2e7895ce620f84fbc35803e4b6da369894a61e75f9ac3b235f`  
		Last Modified: Fri, 22 Nov 2024 20:36:36 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d788db1befe35cc2a6c9a7c8ea813aa50ac5f9ca7a92027f2bf670ed4e23e4fd`  
		Last Modified: Fri, 22 Nov 2024 20:36:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244302a55d960d223d9e1ea84ef1b7413fb7d7902f7498520fca282b6f628a0e`  
		Last Modified: Fri, 22 Nov 2024 20:36:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f74e1ca474eb5bb94c628595d91a57452a8e5b88ff75e1f0a83f4c5778e2e6c`  
		Last Modified: Fri, 22 Nov 2024 20:36:37 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5177c16847945831bb94e1fb3c956b9c5c3855e7119f14a616fdbb834366946`  
		Last Modified: Fri, 22 Nov 2024 20:36:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:807372a6732af95778576063b41bb2b4942afeae3de1a42a860d560a4d967b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 KB (45781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573e7b0c8f4baf0690ba08966c7a1da34062130c556b57bdd9eb83df0d5f18d3`

```dockerfile
```

-	Layers:
	-	`sha256:3156fcfe16b1a39356390bd76bebedee9f88330e6541cf955002e89d535eb2e5`  
		Last Modified: Fri, 22 Nov 2024 20:36:36 GMT  
		Size: 45.8 KB (45781 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:1be1d8189e660b668d2e27f8251b68ca80aa1f1b89a1c52f03aa1c83ab5048bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91838099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d92611a190b6b710252fe1717a9a7ea1f671fba384410fb5bbc192859bc908d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:14:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_MAJOR=16
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_VERSION=16.6
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_SHA256=23369cdaccd45270ac5dcc30fa9da205d5be33fa505e1f17a0418d2caeca477b
# Thu, 21 Nov 2024 20:14:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:14:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:14:24 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:14:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:14:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c21ecb73dc55fd83632acacd41b321b4eaec1e1713eebdb34dd26505cb4f6a9`  
		Last Modified: Tue, 12 Nov 2024 11:43:52 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da6f24cb862024156e04c8278ef84e0343ffffefc262f30e35f293bb46a8cd8`  
		Last Modified: Tue, 12 Nov 2024 11:43:53 GMT  
		Size: 1.1 MB (1086467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d888b7309f123d800f8af6145d64abed32e528f1a44db6bf5788f93a4b0a5a`  
		Last Modified: Tue, 12 Nov 2024 12:31:58 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d840479dd2ab0d81f2a5784be112c99207d6d7c0a4ab7332367973bacf1ed7b0`  
		Last Modified: Tue, 12 Nov 2024 12:26:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb4f75cef72f76fe48ae7d090334d7c58d24df35da1c94346488cc72376b557`  
		Last Modified: Fri, 22 Nov 2024 21:41:21 GMT  
		Size: 87.6 MB (87639405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9072bb46a39d81952e6d5174c3c83defd21d23ce67b2c63d0408b54948ba1e21`  
		Last Modified: Fri, 22 Nov 2024 21:41:19 GMT  
		Size: 9.6 KB (9562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4480d6b2de81551d873762b241593da7e8be847527ebc41ae3e56082c9890888`  
		Last Modified: Fri, 22 Nov 2024 21:41:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0afc3376b5d32d1c23111f6b4ca3d5a1595858d1b6f118c7e1f62662991de9f`  
		Last Modified: Fri, 22 Nov 2024 21:41:19 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d913379902c51c6b54ae2a4c36f31dd5245181965e8f8e9836c2b9ebdaa0631`  
		Last Modified: Fri, 22 Nov 2024 21:41:20 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e538f8c3ff2817ef5fe0a58c8c21314655eb6a101950a0bdabc1f8ab95439b`  
		Last Modified: Fri, 22 Nov 2024 21:41:20 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:c161316b71311a3c568b24bff7cc4b6e41e78774192c22cc9958a22dc32bbcc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.0 KB (637048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc8bb23841b845b26971ae12dd3a41ff89ce7d8cf287f3639d080507102751b`

```dockerfile
```

-	Layers:
	-	`sha256:3dc01d9cb7a4a63c4b7bc8fa1c9e3a9d83d03f0ca6d90695a13e7b58a62fa61c`  
		Last Modified: Fri, 22 Nov 2024 21:41:19 GMT  
		Size: 591.1 KB (591051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c072f8e11db3c7e48b762b862b53349ba65d13e56f5024f5320ecfce17bcbd5`  
		Last Modified: Fri, 22 Nov 2024 21:41:19 GMT  
		Size: 46.0 KB (45997 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:aafc1ed215256b963bcd6ae08cbe43c891c5fe3f5b5f0c0925dba032b1dc9290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98849247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f47c554acc59c5188b80326c9280d1c454fbd17b7f64aa3daed158731e3d599e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:14:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_MAJOR=16
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_VERSION=16.6
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_SHA256=23369cdaccd45270ac5dcc30fa9da205d5be33fa505e1f17a0418d2caeca477b
# Thu, 21 Nov 2024 20:14:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:14:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:14:24 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:14:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:14:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18da34bf685140e836d0db59ef3bd20bbb2e159b50967bc89c4d887c278ced60`  
		Last Modified: Fri, 22 Nov 2024 20:30:42 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c220a87bc36f64e3f6d991339359b63bdeae1796e33611984a43c89c3af99d`  
		Last Modified: Fri, 22 Nov 2024 20:30:43 GMT  
		Size: 1.0 MB (1047256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814866cd64d6d3fcfa8967c97227341dbeb3c0060a3de314dbbf89d8a493493d`  
		Last Modified: Fri, 22 Nov 2024 20:39:09 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aefb335fb518d7fee9719c3bcbc33dd2d038f069e7f27c2ec0068c4a9cd90ad`  
		Last Modified: Fri, 22 Nov 2024 20:39:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b8a6a5f0edcccc6eb55efac4e2e5d24888b0cc4a848847383f9e2c089e21f0`  
		Last Modified: Fri, 22 Nov 2024 20:39:12 GMT  
		Size: 93.7 MB (93697528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4366d55a6b701a2c7b6c64db285965d4dfda221fab7ff999d2049675ff5dec69`  
		Last Modified: Fri, 22 Nov 2024 20:39:10 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e673b5a5705442d58cb6d6cf07d415a513c674fd4549b9dd221142bcef4004a2`  
		Last Modified: Fri, 22 Nov 2024 20:39:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ab582175a2635f1bf0af0124599e27abc8714fad6bda12c020e8ec03393087`  
		Last Modified: Fri, 22 Nov 2024 20:39:10 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c82ff7af5615bc2d7918b9e7ecf1c4fbc2a1758664c06eaaaf614f9840a0d2`  
		Last Modified: Fri, 22 Nov 2024 20:39:11 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6358643cde3ffd9c9eb16d0ccb09b7ec21298bdd81e678d597904d261df672b`  
		Last Modified: Fri, 22 Nov 2024 20:39:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:9a0c8c263a5042d6d232f5e5844943fe3170ad7f9bffe07b6c8c260c1c3d3d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.1 KB (637111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026b12302c52bb197bace8b8c86e40657287a6ed1a5138852a47334defba7eb1`

```dockerfile
```

-	Layers:
	-	`sha256:0e9dc5810260e515a01e3d5cd79f8670f710d139ae4974a43abb3fc72780da25`  
		Last Modified: Fri, 22 Nov 2024 20:39:09 GMT  
		Size: 591.1 KB (591071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d922a533fddd38b5b7a552fcfff63e10cc458cfdf67dfab3fffe74e52fcc504`  
		Last Modified: Fri, 22 Nov 2024 20:39:09 GMT  
		Size: 46.0 KB (46040 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:5e75660aca70a16b290294553a9b9d4f2fefc751bbf3de1aa4cf6e40843b3f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104322403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce4de1d39a3e53a78c6e85c449ddb6a12bd1aacfbe34ff4611530e89facd14b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:14:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_MAJOR=16
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_VERSION=16.6
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_SHA256=23369cdaccd45270ac5dcc30fa9da205d5be33fa505e1f17a0418d2caeca477b
# Thu, 21 Nov 2024 20:14:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:14:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:14:24 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:14:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:14:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258a68a93f860746ca4c897cd73a0c2b70df42999f809b039429a8f908bef4b6`  
		Last Modified: Fri, 22 Nov 2024 20:29:27 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e838dd92729dd98686ce8182c46fad1d9a56012ec426333e737b3c663eec4b22`  
		Last Modified: Fri, 22 Nov 2024 20:29:27 GMT  
		Size: 1.1 MB (1094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6baff4b6c625b20d1800729606679a62ac07fd4240381cf0cde49c0cad19e8c4`  
		Last Modified: Fri, 22 Nov 2024 20:29:27 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b2dfd7b1c97cd0c0d299d628b4914f1761098e73f8f21da455138799973ae6`  
		Last Modified: Fri, 22 Nov 2024 20:29:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93eead371ebb85969863c4674fbdaa2bd3c8a44966987b4e8e03fea3ce7d456`  
		Last Modified: Fri, 22 Nov 2024 20:29:30 GMT  
		Size: 99.7 MB (99741587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02ae486344b3f3352ffd3a18a0d5c1deeaf118df6b6d1a730878920f9198b30`  
		Last Modified: Fri, 22 Nov 2024 20:29:27 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040d737966ee0e86c4d26c8a786cca57010ebc3c65a6c9ec74cc47c7fa04460b`  
		Last Modified: Fri, 22 Nov 2024 20:29:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8127863b0607f40a9ff88fcddcde5c5954121c6fabd266116cbfcef93181c0`  
		Last Modified: Fri, 22 Nov 2024 20:29:28 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce5a0f808636f2551443912281db2cc1e97249ace690ece74eeffd3c08ae57`  
		Last Modified: Fri, 22 Nov 2024 20:29:28 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f11c615d82ed9aee206e32a52c100894d6dc0aa465212f9a5d10dd462a80b6d`  
		Last Modified: Fri, 22 Nov 2024 20:29:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:879acc8d0819eeaa486de455be15727378159c86646523e0861cd3a359f50f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.8 KB (636759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edcd69f24f83f560b9d3a36bb99842e2e9faa346470b8c7a770bb9bc42709da`

```dockerfile
```

-	Layers:
	-	`sha256:f875ce7eb2696e89cffef05dfc7e70e7d495fd3726693893ed4eb60242c90dde`  
		Last Modified: Fri, 22 Nov 2024 20:29:27 GMT  
		Size: 591.0 KB (590990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deed28bc73c53c7d4008ee4936c73fb2a1d3a091834527f30741264cfee0ac82`  
		Last Modified: Fri, 22 Nov 2024 20:29:27 GMT  
		Size: 45.8 KB (45769 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; ppc64le

```console
$ docker pull postgres@sha256:321d652fc53ddc0044a4c57bb4adb28995f3cadb7ca8aa2ba4de63329d2cf1f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103663304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac588400d59990432a9bc0e4884990a275d2328c581898a88d50d15455f31d30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:14:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_MAJOR=16
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_VERSION=16.6
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_SHA256=23369cdaccd45270ac5dcc30fa9da205d5be33fa505e1f17a0418d2caeca477b
# Thu, 21 Nov 2024 20:14:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:14:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:14:24 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:14:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:14:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d839f8f37c77740c639a2d79bcc9196ac00f9a5236d29db68412ccc4b6db1bc`  
		Last Modified: Fri, 22 Nov 2024 20:32:38 GMT  
		Size: 987.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931b910ab9aacc5ec34814d9f698b13ec309cb617273472f1bdbdf837125a96b`  
		Last Modified: Fri, 22 Nov 2024 20:32:38 GMT  
		Size: 1.0 MB (1037936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ef7bc1f7613d2ee66cb656820c84b3d149594db2b1aeb748c6afb244c752ed`  
		Last Modified: Fri, 22 Nov 2024 20:45:42 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40320db15bd0cc752b10795ff6883906af584c842f85a73c9b7d9332ed5e4ff1`  
		Last Modified: Fri, 22 Nov 2024 20:45:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb59e50d004f8ceff5fb499342fbc721268b2f6334c656cefd56db0ddd769bf5`  
		Last Modified: Fri, 22 Nov 2024 20:45:46 GMT  
		Size: 99.0 MB (99036168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc62bd4236d5e5137dce80f3a027cefb367b040b980165f7e4555890ba592005`  
		Last Modified: Fri, 22 Nov 2024 20:45:42 GMT  
		Size: 9.6 KB (9563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff59ef52b6bf842f92c1e57efc5d0e124d2d1cffe6831f1015daa650001f976`  
		Last Modified: Fri, 22 Nov 2024 20:45:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c04f6efe3f438b9bbf9a8c94d184886fbd0973be90dfc1d4da1e264418f67cc`  
		Last Modified: Fri, 22 Nov 2024 20:45:43 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95028ded2ba464fc128de807016be35bb39e7227981890056be16895a76b5340`  
		Last Modified: Fri, 22 Nov 2024 20:45:43 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80908fec1cfa71cd1d1cd72e7feb0c6ccd4add342388543a5fbc66c44e9f484d`  
		Last Modified: Fri, 22 Nov 2024 20:45:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:007ce1b1b22f357e07ad9dbdc07fa1f013299fac8bd537345895533996ca16a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.3 KB (633307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799e86c5e0d79527dc478c24657e9fcb7a4323fe9595c67ff85afc11b5102924`

```dockerfile
```

-	Layers:
	-	`sha256:1c8ccb8a762558ce92b661a2a9eaed55209b036b06a0abb0dee6fdbab947fa8f`  
		Last Modified: Fri, 22 Nov 2024 20:45:42 GMT  
		Size: 587.4 KB (587431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad0b15eea8de69a3059e1a2b23eec58e7f626f1be50d1c975ef66aae1f4f2dfa`  
		Last Modified: Fri, 22 Nov 2024 20:45:42 GMT  
		Size: 45.9 KB (45876 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; riscv64

```console
$ docker pull postgres@sha256:966e8b2a6d38ec895c5c1bd6eee807925a9e846c43ce29aaa2ea612893a731bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (98984607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478ab3df194dca5ae7a4d1a10a81e51a18fdd843b254e3a4e7457eb8458bd950`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:14:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_MAJOR=16
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_VERSION=16.6
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_SHA256=23369cdaccd45270ac5dcc30fa9da205d5be33fa505e1f17a0418d2caeca477b
# Thu, 21 Nov 2024 20:14:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:14:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:14:24 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:14:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:14:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8f6d509c68c45b1fdf0a1a4ab907f53741b31f985f51c20dc23cd8a8d6f8c6`  
		Last Modified: Tue, 12 Nov 2024 20:47:45 GMT  
		Size: 989.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38504f2cb255ba8a48a6b356aaff81feb5626bcddc945bbd59e7de7b2cbad90a`  
		Last Modified: Tue, 12 Nov 2024 20:47:45 GMT  
		Size: 1.1 MB (1087949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e6b162445bb1f4714c82ba5ee78e748e64dab99e6d2b388464c3cc9685b39d`  
		Last Modified: Tue, 12 Nov 2024 21:35:14 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71780435e839b7381f0d933d50d5f447819a9afaac78fd20e751316b070c6534`  
		Last Modified: Tue, 12 Nov 2024 21:35:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9717ae7f6ec7eba7e7501a871a0beb46b85cf9403a8a9ae93206f43ff873f8d3`  
		Last Modified: Fri, 22 Nov 2024 22:15:53 GMT  
		Size: 94.5 MB (94508418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5112cf0486888c234b434dd72b4a632341b75dde4a23926f4a86eef6a867a24`  
		Last Modified: Fri, 22 Nov 2024 22:15:39 GMT  
		Size: 9.6 KB (9569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974aa048597756dde72b0983de3edacd4774d04fddd933c1b209a3e9a7518a9a`  
		Last Modified: Fri, 22 Nov 2024 22:15:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a668d5f64d0d6d9b2112ebe00768b342bdf4db141d2ec89b418291c75da5f2f5`  
		Last Modified: Fri, 22 Nov 2024 22:15:39 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f636516e6211595278de98e700625b6f1c075bb30946e9de9ca5e16a5b761`  
		Last Modified: Fri, 22 Nov 2024 22:15:40 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75faf455f34c998b68fcaad59cec0f985eada3e119b5639375912f6b95924304`  
		Last Modified: Fri, 22 Nov 2024 22:15:40 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:8f731e4375f8010b85d5956dde1330429c5a1a41d97757ebe68941bb4b28ed30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.0 KB (634968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ff62ad13463c6503cd4fa13cbd8f60f358c5e019e2188ff6c10d1b71b160b9`

```dockerfile
```

-	Layers:
	-	`sha256:bb618f4f3cc15c7d25ced0a99424c14ac27adfa3297d2eeb4332329c2d4c5fc9`  
		Last Modified: Fri, 22 Nov 2024 22:15:39 GMT  
		Size: 589.1 KB (589091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cd2a150274f9b94d15ad7c86a8399ba11f9f3e0f0fc6b0daec7f72cfa394f95`  
		Last Modified: Fri, 22 Nov 2024 22:15:38 GMT  
		Size: 45.9 KB (45877 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; s390x

```console
$ docker pull postgres@sha256:c94b91ad3f7845a7d08950ae90974ce3fe2c0d60df6fc31888314fc191dfcd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 MB (107859551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930d43258ff579fef5910bb9ef900408365dcd59e567a74441c4042876a79793`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:14:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_MAJOR=16
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_VERSION=16.6
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_SHA256=23369cdaccd45270ac5dcc30fa9da205d5be33fa505e1f17a0418d2caeca477b
# Thu, 21 Nov 2024 20:14:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:14:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:14:24 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:14:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:14:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111d80413d7dc670023007c293977504f9135ef606bd950d6054183639b4e611`  
		Last Modified: Fri, 22 Nov 2024 20:32:20 GMT  
		Size: 988.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c32b8d57cbf66289af068bbe27152bf640f3ef790357fa33b9081f9125e708`  
		Last Modified: Fri, 22 Nov 2024 20:32:20 GMT  
		Size: 1.1 MB (1083304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be0d0e478d5691eb224ad4c19588349b6c154fcf9071f017da33344d8fac04a`  
		Last Modified: Fri, 22 Nov 2024 20:42:09 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e3194304b7790e364d461f1efc3c2f4a9820a201deb3ef42ce0b5115e042a6`  
		Last Modified: Fri, 22 Nov 2024 20:42:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fa2b4f2cb5367663ee979a598b71f0a6bc05337e58e501a1e41d8c07bf62d6`  
		Last Modified: Fri, 22 Nov 2024 20:42:11 GMT  
		Size: 103.3 MB (103297887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0d7ab4aeeff2c485570bcba47fbd9bec0f1930675bcdb809a517a979c48a78`  
		Last Modified: Fri, 22 Nov 2024 20:42:10 GMT  
		Size: 9.6 KB (9566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994801bb4cce2ce333694db77c240388ae7e6f17e385f07c28dda87130574224`  
		Last Modified: Fri, 22 Nov 2024 20:42:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39684e13f706b369e7b9d05f7da99fae6cdd9b2985eb10b6593b5a55076ffe97`  
		Last Modified: Fri, 22 Nov 2024 20:42:10 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7a6cdfeb1823979cfa5f851cb9b8fc89dcd3ec4bee808896f40bc4a1147a71`  
		Last Modified: Fri, 22 Nov 2024 20:42:11 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2167bb88ea6f7c6eef0b4cea0da2f728d3c87b08b8607c78f0547e4db4823`  
		Last Modified: Fri, 22 Nov 2024 20:42:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:790c48d10ec194fec81124d92714f0f7449fa313867ec7fe3b28fc25a972567b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.9 KB (634884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70a17f8f252610ba6f66fbff8e4f90d854b4ded4b16e7008a532f8a640669d2`

```dockerfile
```

-	Layers:
	-	`sha256:5bb792bb7dee8ade7ddab9a0d6d2d7bc5d18210ac16343921ad98638f2b71202`  
		Last Modified: Fri, 22 Nov 2024 20:42:09 GMT  
		Size: 589.1 KB (589061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d7317e2140cef5f7f537d656f893fdc4206f7a8caec4eea76b0a273b9170f03`  
		Last Modified: Fri, 22 Nov 2024 20:42:09 GMT  
		Size: 45.8 KB (45823 bytes)  
		MIME: application/vnd.in-toto+json
