## `postgres:13-alpine3.17`

```console
$ docker pull postgres@sha256:d61759892463bdbc6105dbebcc4fb5a1a439b7ab0aba5e304a92e239450d806d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `postgres:13-alpine3.17` - linux; amd64

```console
$ docker pull postgres@sha256:5eefe03e06cb3b4d60e955bd30bf05a8520b019ab7df4b8889bea22dbe0689b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94120109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e175ee0192aa95918e42ca6421ba468439ccef7e5487b2379028f288d10553`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Thu, 10 Aug 2023 18:25:03 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:25:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PG_MAJOR=13
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PG_VERSION=13.12
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PG_SHA256=0da1edcee3514b7bc7ba6dbaf0c00499e8ac1590668e8789c50253a6249f218b
# Thu, 10 Aug 2023 18:25:03 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 10 Aug 2023 18:25:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:25:03 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:25:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:25:03 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:25:03 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:25:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10c0392a84957c4940d939463a1c2a3d7e564abf5eafe59d77286fb07e2259f`  
		Last Modified: Fri, 29 Sep 2023 17:15:57 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3adcd9a487a5dae0b31341751e858f863eb761b585f79f7e70d537ebee802b`  
		Last Modified: Fri, 29 Sep 2023 17:09:40 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20647b6a643ac1ccacf10e569d813666c5f7038fa24b5eac3913b1e2ea8bab63`  
		Last Modified: Fri, 29 Sep 2023 17:16:01 GMT  
		Size: 90.7 MB (90726027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea278bff7216f4b491e09f6ecbcdb0ec0f043c673c9199a695fd7cc67d1d2ed`  
		Last Modified: Fri, 29 Sep 2023 17:15:57 GMT  
		Size: 9.0 KB (9020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcec8e3caac2bab3a6b17f80bd959b08fbcdedc9b12faa5cd7c9fcb769e2775`  
		Last Modified: Fri, 29 Sep 2023 17:15:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49d54c2c6b7ab3c274e56409bdc8b4e4062f36bfd98927861cd652c35ea7e74`  
		Last Modified: Fri, 29 Sep 2023 17:15:58 GMT  
		Size: 163.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be34ea5f8c6f62c56e66f8e02bd5828558640b56c17911770baa8c80aaab74b9`  
		Last Modified: Fri, 29 Sep 2023 17:15:58 GMT  
		Size: 4.8 KB (4787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:094d948a6ae6444c7d98984f1851b0d7eee69131b677043939a64727296f1210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ad2d677c1475682568ed99e8dcc78c486450a77fd785ded5b244453f7e7e22`

```dockerfile
```

-	Layers:
	-	`sha256:6d6be5510b2b52745d1009a59ec70b7c5ebf3fe5e823456b6ffe69f8c83c50ce`  
		Last Modified: Fri, 29 Sep 2023 17:15:57 GMT  
		Size: 832.9 KB (832881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4618bbe2e19772921cde45ae90b1bc040e746aeed4c38bfe28012be6687e3332`  
		Last Modified: Fri, 29 Sep 2023 17:15:57 GMT  
		Size: 34.1 KB (34054 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.17` - linux; arm variant v6

```console
$ docker pull postgres@sha256:a03457bf436504cbaeb981c0b128b6f3de7ba813aaa859a51d83c6a46df3c767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91571452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193b0ceb7f48de7854129a44306eecb59013f6a4505b0a21523fd1b0af60e532`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:17 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Mon, 07 Aug 2023 19:49:18 GMT
CMD ["/bin/sh"]
# Thu, 10 Aug 2023 18:25:03 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:25:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PG_MAJOR=13
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PG_VERSION=13.12
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PG_SHA256=0da1edcee3514b7bc7ba6dbaf0c00499e8ac1590668e8789c50253a6249f218b
# Thu, 10 Aug 2023 18:25:03 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 10 Aug 2023 18:25:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:25:03 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:25:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:25:03 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:25:03 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:25:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:342323bc858ed9706f7953ab06cbf6785b678c55ef2317577af748533d11165b`  
		Last Modified: Mon, 07 Aug 2023 19:49:53 GMT  
		Size: 3.1 MB (3112450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762ca12e994065d1b4f88c6c75459b994f7b20e8dfff65b9baaaa81da4e7cd58`  
		Last Modified: Fri, 29 Sep 2023 17:15:50 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6354b86db595db36e6aba08287889de1fd66628548ba2f39de153d50f1b7703`  
		Last Modified: Fri, 29 Sep 2023 17:15:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee9c2b38781a2f0ac2d5f51ad761698120bae8f3a556593e38dce6391e55591`  
		Last Modified: Fri, 29 Sep 2023 17:37:26 GMT  
		Size: 88.4 MB (88443527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7de07be01b27131be43b6569132f84ad0f5eeb49d9358ac1aa336edb8b44cf`  
		Last Modified: Fri, 29 Sep 2023 17:37:14 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c35c42e7373f7b0856cede7c0762b212fc4f30e3a52c07907ef0d7c68b1dea`  
		Last Modified: Fri, 29 Sep 2023 17:37:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05db50ff9bcdc45152c45f45d760f7d227e4ed033f5c52243270f2ab4b217bea`  
		Last Modified: Fri, 29 Sep 2023 17:37:14 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb35c642ec66034ec03712bdc568f05a6955cf9f7aff473ff8a0edf940224578`  
		Last Modified: Fri, 29 Sep 2023 17:37:14 GMT  
		Size: 4.8 KB (4785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine3.17` - linux; arm variant v7

```console
$ docker pull postgres@sha256:4989bf6643e1b64271f760f5a5c0109c2ef098fb510f55ed927ef58bb7a77019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86157562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a88e1fc220c705d655e2d19681e0d024d57b684337d23cd88c6d96f5d96057`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:29 GMT
ADD file:7f36c30ba2b714d09a8650dba1545abdf892443dadbe9113b9a166b84ba7ac3f in / 
# Mon, 07 Aug 2023 19:57:29 GMT
CMD ["/bin/sh"]
# Thu, 10 Aug 2023 18:25:03 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:25:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PG_MAJOR=13
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PG_VERSION=13.12
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PG_SHA256=0da1edcee3514b7bc7ba6dbaf0c00499e8ac1590668e8789c50253a6249f218b
# Thu, 10 Aug 2023 18:25:03 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 10 Aug 2023 18:25:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:25:03 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:25:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:25:03 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:25:03 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:25:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b82e4fd40279a40aa2eecd301fabb2dca254727cc09daa8d0caf69ac28c44af1`  
		Last Modified: Mon, 07 Aug 2023 19:58:08 GMT  
		Size: 2.9 MB (2869425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86a7e0ceec6ac99871591a1aeebc1fd8de1c7033f6d90cb86a191ae38248d6f`  
		Last Modified: Fri, 29 Sep 2023 17:55:30 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8311cff793f98bd132193590d9e83c991b2a2357d7abaf5945629eb6ce6b6796`  
		Last Modified: Fri, 29 Sep 2023 17:55:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6ae6eb0559f9a3182ac1243b7f8acc48e81fa64bd1523ed9b79a2a65335b75`  
		Last Modified: Fri, 29 Sep 2023 23:13:11 GMT  
		Size: 83.3 MB (83272663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59534a081e9cedfa402720e85864b23cd0aaba0a0d3922be9be7954da51813c`  
		Last Modified: Fri, 29 Sep 2023 23:13:07 GMT  
		Size: 9.0 KB (9019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada70d012a809d04b618d04b597bdb0d7901f211340c37ee131f35703a22f96b`  
		Last Modified: Fri, 29 Sep 2023 23:13:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306618c5adaf9916f52d70153c17fb092adef4da930482c06c1bc985550295e7`  
		Last Modified: Fri, 29 Sep 2023 23:13:07 GMT  
		Size: 163.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8364fc7c85767b8faa02b4b016dc21ea80a96537e2b6b8d8c577930ff3889b8b`  
		Last Modified: Fri, 29 Sep 2023 23:13:08 GMT  
		Size: 4.8 KB (4785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:7a5ee506ffce15ceb6c9c26f1d6930fd7ce73087efffd059b36388f0364a1c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fb06d7d85f44a24bf4c1c313adf13c59f8613191de0ea2a37f6890148ef213`

```dockerfile
```

-	Layers:
	-	`sha256:7fc14e7a716dba0745d39814355147609bf4ccbf0c6d38bd0dbb95f36169f147`  
		Last Modified: Fri, 29 Sep 2023 23:13:06 GMT  
		Size: 832.9 KB (832899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f59c1336ab7ecf558e94aaba45fcb248c2dc5a90b757cedff09327dd3c56e067`  
		Last Modified: Fri, 29 Sep 2023 23:13:06 GMT  
		Size: 34.0 KB (34007 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:093954f652cabd240a4aa67a2bfd7bfbe7cc0183a54ed7182541e3b6767c67ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91742576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9f4528b13c4d6e18f03472cf0895890176cb41e25415ab12200fbf597431f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Thu, 10 Aug 2023 18:25:03 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:25:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PG_MAJOR=13
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PG_VERSION=13.12
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PG_SHA256=0da1edcee3514b7bc7ba6dbaf0c00499e8ac1590668e8789c50253a6249f218b
# Thu, 10 Aug 2023 18:25:03 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 10 Aug 2023 18:25:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:25:03 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:25:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:25:03 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:25:03 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:25:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4060ece20d7ac783f52cbe28a35fd5b06f90f7b4d773bae0d956024e85ff35b6`  
		Last Modified: Mon, 07 Aug 2023 19:39:59 GMT  
		Size: 3.3 MB (3258290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66afaa819c151e5c140f0003d5597cc280c5940afb92086efa5bd614b7250dab`  
		Last Modified: Fri, 29 Sep 2023 17:17:20 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51fa533ac9f9fc7f59abce0691c3def21d591b52ebbfb89415d63fe927fe8fb`  
		Last Modified: Fri, 29 Sep 2023 17:17:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cb8343b5ca604b717f70daed533198d47c641c4cbf8e0770e8dc855cafafa2`  
		Last Modified: Fri, 29 Sep 2023 17:38:39 GMT  
		Size: 88.5 MB (88468807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2903dbfa3dd99f2c74c873f04ef513092998d2a98e2d2eb9a4ed9ecbeb779273`  
		Last Modified: Fri, 29 Sep 2023 17:38:34 GMT  
		Size: 9.0 KB (9022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ad4956b80809f0c94429682bebaaa2c54febec1a726e14b0cd0dca7b61ea35`  
		Last Modified: Fri, 29 Sep 2023 17:38:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e339f51ec23607cac2e97a2e555c22b87b2baf00283cc4e16a4db2fd6f6fc48`  
		Last Modified: Fri, 29 Sep 2023 17:38:34 GMT  
		Size: 163.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee334fdc6815e42f20814ccfd62f9a2b597f30356884d3a104db9313e4bc7c49`  
		Last Modified: Fri, 29 Sep 2023 17:38:35 GMT  
		Size: 4.8 KB (4788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:22a1d696ae1029f736b3800c8c8d8a3a57aacc60d1a197b6475f493f3d014ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ced4361eb5c281f217187f41aefdbe9428d019366083e48339ce5773ab732a6`

```dockerfile
```

-	Layers:
	-	`sha256:82374af7b1a9b7e8ede35cc6c5947b5c88358ce089595f9906984813d6b49b22`  
		Last Modified: Fri, 29 Sep 2023 17:38:35 GMT  
		Size: 832.9 KB (832890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:986560b226557f9209c20ac48911351097bd4cb827218ffcc87dd0c2a188ccc5`  
		Last Modified: Fri, 29 Sep 2023 17:38:34 GMT  
		Size: 33.9 KB (33894 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.17` - linux; 386

```console
$ docker pull postgres@sha256:90a436bfa7ffffc9821ff1dfa73a02e2ffb8d1d22a7916708f9ed7ecca6b8261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98897087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24223210a8d5b0164716703631417afb0bef08e9c9afdbceecccadd64979b3a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:30 GMT
ADD file:437e2411fa3e4795a759f54507f41caa000169f0c32600ec49b4397313cd0884 in / 
# Mon, 07 Aug 2023 19:38:30 GMT
CMD ["/bin/sh"]
# Thu, 10 Aug 2023 18:25:03 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:25:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PG_MAJOR=13
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PG_VERSION=13.12
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PG_SHA256=0da1edcee3514b7bc7ba6dbaf0c00499e8ac1590668e8789c50253a6249f218b
# Thu, 10 Aug 2023 18:25:03 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 10 Aug 2023 18:25:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:25:03 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:25:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:25:03 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:25:03 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:25:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ddc7d64c528fabaad61cc880e91abba829973f743d753415145211971f9ee10d`  
		Last Modified: Mon, 07 Aug 2023 19:39:10 GMT  
		Size: 3.4 MB (3413779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd16067e5f3f75d308dc48788eba491793c9d599fc6c6d7ad767e6c09127d20`  
		Last Modified: Fri, 29 Sep 2023 17:15:21 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e5d0575df3654e747d1cf297ebbc56a42afac2b31cfcd75c6277a0bacc9b73`  
		Last Modified: Fri, 29 Sep 2023 17:15:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7f2413fe07e904bf543aee11ebbb7c38d3e1818a6ecd999d2149df3f88181f`  
		Last Modified: Fri, 29 Sep 2023 17:15:27 GMT  
		Size: 95.5 MB (95467835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391fabfca3a45849964ebf211b22e2dbb392b1b106d0be05adb1e75f9a0d9d4f`  
		Last Modified: Fri, 29 Sep 2023 17:15:22 GMT  
		Size: 9.0 KB (9020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7462336cdfb24b02a8d645afdeffe99419f2300eafec35fabfca34fbf13d9b6a`  
		Last Modified: Fri, 29 Sep 2023 17:15:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d37e6be07d7f19ce86ddcd6085bf4a3aa594d43aae183af0c0d31d92d3e688e`  
		Last Modified: Fri, 29 Sep 2023 17:15:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7c5bb12c3d90017ec11b8e1b696bef783e4566033438a8bdeb6fd72bf5627b`  
		Last Modified: Fri, 29 Sep 2023 17:15:22 GMT  
		Size: 4.8 KB (4787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:4d95d5755aafcb2160a577d4e88cdb81df7834aa828671ebc3123c9d1a43b906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 KB (33810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b167f1d45417684a5a00da21ca40de84ba2cda4ea162690622ed7a013ab749b`

```dockerfile
```

-	Layers:
	-	`sha256:d47d7f5ca89fb124c6b0ce8647228541d12e4d0732e96ae4a2a26f8b2d6e5f62`  
		Last Modified: Fri, 29 Sep 2023 17:15:21 GMT  
		Size: 33.8 KB (33810 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.17` - linux; ppc64le

```console
$ docker pull postgres@sha256:328e191f5d62cc2b185b295ee71d26d21c40a32a37aa0240a0228d05643fb185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99764328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6937913417306ce4c73e9001ac513d0cd29c4a7cca21d3c9c7bc8a4dac429a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:35 GMT
ADD file:52f28bcdd6e1c6f85b2b5d66ace37ed6cef0da8ce5c58e246549427361b64c1d in / 
# Mon, 07 Aug 2023 20:16:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Aug 2023 18:25:03 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:25:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PG_MAJOR=13
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PG_VERSION=13.12
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PG_SHA256=0da1edcee3514b7bc7ba6dbaf0c00499e8ac1590668e8789c50253a6249f218b
# Thu, 10 Aug 2023 18:25:03 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 10 Aug 2023 18:25:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:25:03 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:25:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:25:03 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:25:03 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:25:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1e00d0a2a797866697ccca7b6307a9182e2852583b2b3be3928d196e4cb8ba3d`  
		Last Modified: Mon, 07 Aug 2023 20:17:39 GMT  
		Size: 3.4 MB (3391349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5b974f36ada4db166b317dbd7ec8b2b88b37937068c28d805d09538326d90c`  
		Last Modified: Fri, 29 Sep 2023 17:25:31 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcac4460d7aac564d0ebb57321859304cbf7b78467b55bb8ba1882b22818990`  
		Last Modified: Fri, 29 Sep 2023 17:25:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57617989483b45e1d6462ad3df7e76a406c085c5d2bfd413a27f74d5d6499d71`  
		Last Modified: Fri, 29 Sep 2023 18:03:17 GMT  
		Size: 96.4 MB (96357489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac514f2ca486d60aa68e70091ee111475ed78f1362e837506b05e64dc6c557b8`  
		Last Modified: Fri, 29 Sep 2023 18:03:10 GMT  
		Size: 9.0 KB (9028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a694d92d6ae40f0dd2c86a43840b669e56cd36a093cfee577a74ffd8b5ff38`  
		Last Modified: Fri, 29 Sep 2023 18:03:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2929deff526d06648474970d8daaedaae6bc3a5da656c9c71297a54448dd83`  
		Last Modified: Fri, 29 Sep 2023 18:03:11 GMT  
		Size: 164.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d1a4c4960d19e369cda2fb57c33c48845c121ea0c2a6793f564225a471451b`  
		Last Modified: Fri, 29 Sep 2023 18:03:12 GMT  
		Size: 4.8 KB (4787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:65cd41fc77aaca47c76eb5ad4f35349b9f309697ac80849eca849306ab45286e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **863.4 KB (863398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1aedea08b2e97a90076104b93642c8abb3ae2b74621fa5556b1d4fc3e4f7683`

```dockerfile
```

-	Layers:
	-	`sha256:0564d53399cd8585feafd98dcccc69dceefeea75ec7780ae8e4b31084b563b56`  
		Last Modified: Fri, 29 Sep 2023 18:03:11 GMT  
		Size: 829.5 KB (829474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67ddd7ec0ba2b951c6819243861feba7bde5d6cca182e1ca6205f5bee8bf692f`  
		Last Modified: Fri, 29 Sep 2023 18:03:10 GMT  
		Size: 33.9 KB (33924 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.17` - linux; s390x

```console
$ docker pull postgres@sha256:0c873554b587245c6bc6d1817d30eca534f3d483fc8d7b91ede21ae4164c45d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94371528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17763c28e691ea49c916d6c8520effafa34a69041f408c99d4047c527e0401fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:42:01 GMT
ADD file:2e221805acb91c51e7afa6b926252ab2260cdf2e166f3d917a98384f3a157622 in / 
# Mon, 07 Aug 2023 19:42:02 GMT
CMD ["/bin/sh"]
# Thu, 10 Aug 2023 18:25:03 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:25:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PG_MAJOR=13
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PG_VERSION=13.12
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PG_SHA256=0da1edcee3514b7bc7ba6dbaf0c00499e8ac1590668e8789c50253a6249f218b
# Thu, 10 Aug 2023 18:25:03 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 10 Aug 2023 18:25:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:25:03 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:25:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:25:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:25:03 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:25:03 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:25:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b69f31b9e61dae76a66eb3f9dd10f9f86d10116c6339347c47739dcf850af4d3`  
		Last Modified: Mon, 07 Aug 2023 19:42:48 GMT  
		Size: 3.2 MB (3175974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd127ab918326354fabf67e5ea3a64351cd5ead4351072a4975ecdad37b818ed`  
		Last Modified: Fri, 29 Sep 2023 17:41:19 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241ad07c08f6393e1d618505c97ba7bb90a83336aab71cc4ce44365a03db1cbd`  
		Last Modified: Fri, 29 Sep 2023 17:41:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9542c134e20b376c7f5304cbf83154a7f48edc4bfd342c15e8fbb0fc52af4f15`  
		Last Modified: Fri, 29 Sep 2023 18:38:50 GMT  
		Size: 91.2 MB (91180066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c3792bcc57de5cb64a4eccac133730714fc3d5f049c40dcc743f9412d1d627`  
		Last Modified: Fri, 29 Sep 2023 18:38:45 GMT  
		Size: 9.0 KB (9029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3163ffa5dd7d8c2ca3e92822e1c0227d30789b858f6f5e3597900576de35658b`  
		Last Modified: Fri, 29 Sep 2023 18:38:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56eb01a5c79f27dd1ab32e0bcc5e107ec95bc712301aa10c2acafb64011fa7e9`  
		Last Modified: Fri, 29 Sep 2023 18:38:45 GMT  
		Size: 163.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac6db4e09e747c362d69e20e5592f492bf5bbc4ba55ef4a60ef3ec42127d9e4`  
		Last Modified: Fri, 29 Sep 2023 18:38:46 GMT  
		Size: 4.8 KB (4787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:86210c03d1ebb35b9d3694aa83d18def6b4621248fb0219c73b1701f80f7073f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **864.8 KB (864837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703579e6c1381ec2d36646a38b5636682abc67dcf10adeb79b416b94bb491450`

```dockerfile
```

-	Layers:
	-	`sha256:8901fc6a39c0bc847ee764960319b98ef392c76afc990e93e9e12d2cafc37c3f`  
		Last Modified: Fri, 29 Sep 2023 18:38:45 GMT  
		Size: 830.9 KB (830949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84356aa873b099d4041b2d71b968c6e2eb3fc7605cdd80acfa3dbab97da6c4f0`  
		Last Modified: Fri, 29 Sep 2023 18:38:45 GMT  
		Size: 33.9 KB (33888 bytes)  
		MIME: application/vnd.in-toto+json
