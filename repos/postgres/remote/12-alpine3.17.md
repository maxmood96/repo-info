## `postgres:12-alpine3.17`

```console
$ docker pull postgres@sha256:7f736925d906ea766b8c5cacdbc9bb237eda0d2bc0bb7b6c11be74c236ad05ec
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

### `postgres:12-alpine3.17` - linux; amd64

```console
$ docker pull postgres@sha256:f12df62d9bfd89488110ad9fa015e4e44f269e0d04447cc476743481f7e4c718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93422395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3a11d923d994a2f4b84ea0595bd700f4f281b492456647ec78d851809d4d95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Thu, 10 Aug 2023 18:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PG_MAJOR=12
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PG_VERSION=12.16
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PG_SHA256=c5f1fff7a0f93e1ec3746417b0594290ece617b4995ed95b8d527af0ba0e38f3
# Thu, 10 Aug 2023 18:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 10 Aug 2023 18:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:14:30 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:14:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:14:30 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8336a8b7f468c07a479c33be81e0c162f1d0e2bf880cc2982e87393e9e7881f`  
		Last Modified: Fri, 29 Sep 2023 17:14:43 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e1b18769deb6f167a54d65b2cf4709a51e84d596986268d2c2a607c510edbc`  
		Last Modified: Fri, 29 Sep 2023 17:14:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8415c2897b26f8cad1f0f757b573f5d3f01c73c041063b53432ddbae2a3d87`  
		Last Modified: Fri, 29 Sep 2023 17:14:48 GMT  
		Size: 90.0 MB (90028643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0590fa04f8d9ed48793d8ca4d20c2ea2ad6972e02d9b3516e0d5b55d95d6c78`  
		Last Modified: Fri, 29 Sep 2023 17:14:44 GMT  
		Size: 8.7 KB (8688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf1ab96e7f1db06677b9f3111bcc2a85fd0683bee2deef5dffe44a2cf837cb7`  
		Last Modified: Fri, 29 Sep 2023 17:14:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb26e72f9b55f99c7a9c3bd4d9a4f783a155fd19afbd43a79f06d4b751b15779`  
		Last Modified: Fri, 29 Sep 2023 17:14:44 GMT  
		Size: 163.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d39bc48fa2e70071eaa858907d4119fbcde75f8fa2052859b4aa1de276aa0d4`  
		Last Modified: Fri, 29 Sep 2023 17:14:45 GMT  
		Size: 4.8 KB (4785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:db1980311e48d56095db7daf6dda5942502a10df6f632cc752dbf31fe10fffdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4536b157d496024a7d43531572fd56ee673ddd0784e2eee9f00a1a60c1de2a46`

```dockerfile
```

-	Layers:
	-	`sha256:48a4a83fc22be3793379026437c93ddc69cf85eeee40b9ea086b13fb978d57ab`  
		Last Modified: Fri, 29 Sep 2023 17:14:43 GMT  
		Size: 832.9 KB (832881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c231cce8944331760fdea96ce436c92605cc2c18544b3e528c639440e736771`  
		Last Modified: Fri, 29 Sep 2023 17:14:43 GMT  
		Size: 34.1 KB (34052 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.17` - linux; arm variant v6

```console
$ docker pull postgres@sha256:cbd9b29469053c33dc060efd31af25537c8909bb39555a5c4706d191c1be76ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (90974725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd17a613614751e410d2f385d7fa772a11665ed5de39bb4ecb6a0f088ba24541`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:17 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Mon, 07 Aug 2023 19:49:18 GMT
CMD ["/bin/sh"]
# Wed, 04 Oct 2023 14:54:45 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
ENV LANG=en_US.utf8
# Wed, 04 Oct 2023 14:54:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_MAJOR=12
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_VERSION=12.16
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_SHA256=c5f1fff7a0f93e1ec3746417b0594290ece617b4995ed95b8d527af0ba0e38f3
# Wed, 04 Oct 2023 14:54:45 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 04 Oct 2023 14:54:45 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"12.16","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@12.16?os_name=alpine&os_version=3.17"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 04 Oct 2023 14:54:45 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 04 Oct 2023 14:54:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Oct 2023 14:54:45 GMT
STOPSIGNAL SIGINT
# Wed, 04 Oct 2023 14:54:45 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 04 Oct 2023 14:54:45 GMT
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
	-	`sha256:2a503fb411748b6ce405e61e9786983d4155fa92fcd9f71464499978d6a0d717`  
		Last Modified: Fri, 06 Oct 2023 01:41:31 GMT  
		Size: 87.8 MB (87847134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c18d66a94e729a86a5d3dbe6111b4bfb3e402552736a475c8c6359c82ef1a43`  
		Last Modified: Fri, 06 Oct 2023 01:41:19 GMT  
		Size: 8.7 KB (8686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb14b6e2eec4a1379d7dd47b89f673bc9c53922b48a01e4c098b178967c6ca00`  
		Last Modified: Fri, 06 Oct 2023 01:41:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7fe0d51468b780f6c2eadb0843dd1ce072acac443bf5a0647aa1e11f94425f`  
		Last Modified: Fri, 06 Oct 2023 01:41:19 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5d0370c173ea2c136853a2e48495ebbc7f9c70da9751b0272b58a0d7a8c2c1`  
		Last Modified: Fri, 06 Oct 2023 01:41:20 GMT  
		Size: 4.8 KB (4784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine3.17` - linux; arm variant v7

```console
$ docker pull postgres@sha256:39dc4d09758fa7d56c098bbf38ea0a144d9e89de422be567a3629cec178df421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85580756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e92086d0e4e354c96d74ba7a50678d131fdcf2a7037d9919d1dc10572e2bffc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:29 GMT
ADD file:7f36c30ba2b714d09a8650dba1545abdf892443dadbe9113b9a166b84ba7ac3f in / 
# Mon, 07 Aug 2023 19:57:29 GMT
CMD ["/bin/sh"]
# Thu, 10 Aug 2023 18:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PG_MAJOR=12
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PG_VERSION=12.16
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PG_SHA256=c5f1fff7a0f93e1ec3746417b0594290ece617b4995ed95b8d527af0ba0e38f3
# Thu, 10 Aug 2023 18:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 10 Aug 2023 18:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:14:30 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:14:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:14:30 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:14:30 GMT
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
	-	`sha256:3a5eb419485ec5348375f67c4749b6f351df3bfb4a4a13fbb1f5fe6a0972a777`  
		Last Modified: Sat, 30 Sep 2023 00:04:26 GMT  
		Size: 82.7 MB (82696187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03f29a7424c99c2b58051bd501dbf9bebf0f546057e10e7a214b61b86c1a345`  
		Last Modified: Sat, 30 Sep 2023 00:04:21 GMT  
		Size: 8.7 KB (8690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8c74ac7d039e7adf3c79f312db962e4f96f196ad57bdbf7902382faa3ffa7b`  
		Last Modified: Sat, 30 Sep 2023 00:04:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8d15927e8cf64086ce1e09d977f1cc9a6b96d2a6d790bdc1d0cd2af7c00b5b`  
		Last Modified: Sat, 30 Sep 2023 00:04:21 GMT  
		Size: 163.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6c2831e403c424cde517bae10a9ca0e65025462748a7b977f130852b7c2194`  
		Last Modified: Sat, 30 Sep 2023 00:04:22 GMT  
		Size: 4.8 KB (4784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:07a1a182306d58ae76d589fb2892fb93749f4f7e53fc3d240a7b36dae9874b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b4a5ea1508b51e13d92c4fda2dabf66980953e9bde43e5a92f710cb633a3f2b`

```dockerfile
```

-	Layers:
	-	`sha256:d6817261792b8194c50fc840546355537a26f6370f3c33cea79ffeb99b05682e`  
		Last Modified: Sat, 30 Sep 2023 00:04:21 GMT  
		Size: 832.9 KB (832899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:416874752f92da7f14d77a26087a98640adff82b57e7727115a54621017bf6c8`  
		Last Modified: Sat, 30 Sep 2023 00:04:20 GMT  
		Size: 34.0 KB (34007 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:fd55ba628a173d9e3925496a72cc026cc40e1b4636cda61480335fa82c73e9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91104395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b53502d839479f30cfb88581f45a41d6fccde745410340717bc4b23a66b546a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Thu, 10 Aug 2023 18:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PG_MAJOR=12
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PG_VERSION=12.16
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PG_SHA256=c5f1fff7a0f93e1ec3746417b0594290ece617b4995ed95b8d527af0ba0e38f3
# Thu, 10 Aug 2023 18:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 10 Aug 2023 18:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:14:30 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:14:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:14:30 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:14:30 GMT
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
	-	`sha256:f0f736e31b57cacfd0822c6742751ad50504b70c1fa4d942b8133430fe0ea429`  
		Last Modified: Fri, 29 Sep 2023 17:45:11 GMT  
		Size: 87.8 MB (87830962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12855a20600f09ba4308a22a3e2a8b18f8d5d9d5b74b7c7726c310422f771a4`  
		Last Modified: Fri, 29 Sep 2023 17:45:06 GMT  
		Size: 8.7 KB (8688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ac52132c6b19452f61ba7f4bfc9a671a077dd4c20fef8e21388c5f94d9aba1`  
		Last Modified: Fri, 29 Sep 2023 17:45:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d519b56b0772dce60658cb08cdd30e8d6a66a1359b3879fc1a97ec4a10213305`  
		Last Modified: Fri, 29 Sep 2023 17:45:07 GMT  
		Size: 163.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cea53e7909a4845a7e6332ca10d649eeb3bd8ad7d1de551c46876ef051857d6`  
		Last Modified: Fri, 29 Sep 2023 17:45:08 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:1c3f6c2c456cf20a8e0b5ffeec6b336d7c03da2f6a7ce2cd574181b6f45efbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00d329511b24557636292afd80d05055d05d5ca690a73b5138c7d16e6999e0c`

```dockerfile
```

-	Layers:
	-	`sha256:82742a4d4ec6a00312b15ffaec91e9184c65bae433955d9ff729598a799875ab`  
		Last Modified: Fri, 29 Sep 2023 17:45:07 GMT  
		Size: 832.9 KB (832890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f8013a20db4b0c56ffb4e3a67757bcd556c326475eafe231cc1ea167366bdd4`  
		Last Modified: Fri, 29 Sep 2023 17:45:06 GMT  
		Size: 33.9 KB (33894 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.17` - linux; 386

```console
$ docker pull postgres@sha256:f441315e4f3ea337e254f0d22607c80afb01694700405140c3e2b2f46e84076c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98187086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced006814e22b901b8c7caf97e3c479d77e9ebbb202aa6d83eb9f17b2337899e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:30 GMT
ADD file:437e2411fa3e4795a759f54507f41caa000169f0c32600ec49b4397313cd0884 in / 
# Mon, 07 Aug 2023 19:38:30 GMT
CMD ["/bin/sh"]
# Thu, 10 Aug 2023 18:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PG_MAJOR=12
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PG_VERSION=12.16
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PG_SHA256=c5f1fff7a0f93e1ec3746417b0594290ece617b4995ed95b8d527af0ba0e38f3
# Thu, 10 Aug 2023 18:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 10 Aug 2023 18:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:14:30 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:14:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:14:30 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ddc7d64c528fabaad61cc880e91abba829973f743d753415145211971f9ee10d`  
		Last Modified: Mon, 07 Aug 2023 19:39:10 GMT  
		Size: 3.4 MB (3413779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b55cef023aacc3918b5ddb38ae67355ee100f7ff1a27101d80e8e354217771`  
		Last Modified: Fri, 29 Sep 2023 17:17:56 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd884fa604b3f4f6bfb697d9be8ebc5aad1eda2ba73a4a441bffe5fe5969deca`  
		Last Modified: Fri, 29 Sep 2023 17:17:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9eb6f4cdd8f9f03aaf624b6c16d3c27abefb4a7c99fd4923a8c4b33f477d16e`  
		Last Modified: Fri, 29 Sep 2023 17:18:01 GMT  
		Size: 94.8 MB (94758155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d11a57b55c5786fce442768ad43ff7a42bfc77db80295a761a6f06dd1087bf`  
		Last Modified: Fri, 29 Sep 2023 17:17:56 GMT  
		Size: 8.7 KB (8693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcf9deb553e2a3bbd338fed34b576b60aefb3eabc7d40b1621ec36980455ab0`  
		Last Modified: Fri, 29 Sep 2023 17:17:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a15a242bb9d1731b7ccc83d1965c202cdf52040f47c8c32fa31a0076e513981`  
		Last Modified: Fri, 29 Sep 2023 17:17:57 GMT  
		Size: 163.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ab02e4a95321ad6828013f70d0536d26ea613f75408edb0fdf476df52cd225`  
		Last Modified: Fri, 29 Sep 2023 17:17:57 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:0668f693edbb1b3d1f644235a0e6a7209d6a6ec9db9f6e4ad06fd792b208d973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 KB (33810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb3be2e4576a97b14ad25f0c711e7521fdf0d932c555dccff29710e35c61479`

```dockerfile
```

-	Layers:
	-	`sha256:ffcc5bbf48301bd8ff4095845c7b57ad2a3205dae4322b9a00def7ed63a78f0c`  
		Last Modified: Fri, 29 Sep 2023 17:17:56 GMT  
		Size: 33.8 KB (33810 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.17` - linux; ppc64le

```console
$ docker pull postgres@sha256:e979ffaafdc126b9dcc32fbeea2957b92afcd68f4b41435a85a90d330cb0f20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99050545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db07117c709abfe2acdb221dc3b8d5fe815671fae1a1be0df2b8547b5e6960e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:35 GMT
ADD file:52f28bcdd6e1c6f85b2b5d66ace37ed6cef0da8ce5c58e246549427361b64c1d in / 
# Mon, 07 Aug 2023 20:16:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Aug 2023 18:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PG_MAJOR=12
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PG_VERSION=12.16
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PG_SHA256=c5f1fff7a0f93e1ec3746417b0594290ece617b4995ed95b8d527af0ba0e38f3
# Thu, 10 Aug 2023 18:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 10 Aug 2023 18:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:14:30 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:14:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:14:30 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:14:30 GMT
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
	-	`sha256:5ce553fc7901058eff95cf0e94e324d3881947a98d24741030b1370710f63126`  
		Last Modified: Fri, 29 Sep 2023 18:18:25 GMT  
		Size: 95.6 MB (95644036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87870aa02270171b106907664a89a4b19c44ad327ec720e5167b606b0955efa`  
		Last Modified: Fri, 29 Sep 2023 18:18:21 GMT  
		Size: 8.7 KB (8696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb80366a4cd82c0ecc13c1edeffd12be00acaea660c34a635a95da7aadc2d7ee`  
		Last Modified: Fri, 29 Sep 2023 18:18:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62152b9a4b102e66c3a5b4085fbf19938389df93984be891a8e6094e26deb61b`  
		Last Modified: Fri, 29 Sep 2023 18:18:21 GMT  
		Size: 163.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0fb9e9a2dfd755326a0202cb2fc404ded22412ae23d57eee15fc75fd5843d`  
		Last Modified: Fri, 29 Sep 2023 18:18:22 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:ce937662a1cfe4633ba3bf690a7a75523789f6d0ebb7e09f4b0c7a7aafe2e119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **863.4 KB (863398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64656abb3ae6137185ae2017bf996b87e69d431098808d013b2ffa0e763ae710`

```dockerfile
```

-	Layers:
	-	`sha256:e0e285e72c83061558691cfa6e7f08da52feb2345a53078dc178a483135628fb`  
		Last Modified: Fri, 29 Sep 2023 18:18:21 GMT  
		Size: 829.5 KB (829474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afa170138171524114f3965146cc95c69b0dce26dd68357f1219c43f208c680b`  
		Last Modified: Fri, 29 Sep 2023 18:18:21 GMT  
		Size: 33.9 KB (33924 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.17` - linux; s390x

```console
$ docker pull postgres@sha256:f1ff6c87bf600ba81e5856aad3318d23be65ab7ed6143fdc67252fbf1d55f0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93645654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c796774e2bf2222fe3008ce99b5f4011e563adea8c4d8c497d1189cddea5e290`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:42:01 GMT
ADD file:2e221805acb91c51e7afa6b926252ab2260cdf2e166f3d917a98384f3a157622 in / 
# Mon, 07 Aug 2023 19:42:02 GMT
CMD ["/bin/sh"]
# Thu, 10 Aug 2023 18:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PG_MAJOR=12
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PG_VERSION=12.16
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PG_SHA256=c5f1fff7a0f93e1ec3746417b0594290ece617b4995ed95b8d527af0ba0e38f3
# Thu, 10 Aug 2023 18:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 10 Aug 2023 18:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:14:30 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:14:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:14:30 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:14:30 GMT
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
	-	`sha256:cbf54f858dfca7a43f7c42507703ece2fd04ca85c7a9e37c279c486a6a568901`  
		Last Modified: Fri, 29 Sep 2023 18:48:05 GMT  
		Size: 90.5 MB (90454525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c77b1de7453081ce69923853aad609e4abe1c478c27f42bed8b8bf9741b236b`  
		Last Modified: Fri, 29 Sep 2023 18:48:01 GMT  
		Size: 8.7 KB (8697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a2c29f3e66a74a6d5090800d169a3f1759f50db38a4551820e67c6c4e1d30`  
		Last Modified: Fri, 29 Sep 2023 18:48:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9eecd40cd9221fea1ad0af457f2142be3b47f20242ab35e1a298cacaff78bf9`  
		Last Modified: Fri, 29 Sep 2023 18:48:01 GMT  
		Size: 163.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f514095bd9e0580d6416681517543edcc9b940a393827e3afef10966528cd186`  
		Last Modified: Fri, 29 Sep 2023 18:48:02 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:9f386545c9485638f0d29a3554272f9bb0c9c589e8559654a6f814f82a8db842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **864.8 KB (864837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab4c4cdeefd51de3a19fda222bf8d7b39de8733a82a63b51ec02cf37be2e065`

```dockerfile
```

-	Layers:
	-	`sha256:482f1757296c411d699465d5d6bb0bb6619c87bd484dc7bb23eacea0fe0a3527`  
		Last Modified: Fri, 29 Sep 2023 18:48:01 GMT  
		Size: 830.9 KB (830949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ebf761264c1c187be307d767f83d546cceac828dd050e9599b7427e02621d2`  
		Last Modified: Fri, 29 Sep 2023 18:48:01 GMT  
		Size: 33.9 KB (33888 bytes)  
		MIME: application/vnd.in-toto+json
