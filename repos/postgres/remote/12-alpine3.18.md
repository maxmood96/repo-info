## `postgres:12-alpine3.18`

```console
$ docker pull postgres@sha256:88077d4ff5e67742593a1982341b9c030cd1c3a435b8ea0098347b33703f80a6
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

### `postgres:12-alpine3.18` - linux; amd64

```console
$ docker pull postgres@sha256:0f09d37b9601b00387055857f0b3b9e6419b268294d58c09571114b7dcf9f95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90535944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3f8389ec56e3f303b00b87fd3bfb3efda014b682639067b0b9219e6b965ebf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 Nov 2023 19:16:09 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 09 Nov 2023 19:16:09 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 19:16:09 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 19:16:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PG_MAJOR=12
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PG_VERSION=12.17
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PG_SHA256=93e8e1b23981d5f03c6c5763f77b28184c1ce4db7194fa466e2edb65d9c1c5f6
# Thu, 09 Nov 2023 19:16:09 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 Nov 2023 19:16:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"12.17","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@12.17?os_name=alpine&os_version=3.18"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 19:16:09 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 19:16:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 19:16:09 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 19:16:09 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 19:16:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826c0ef9718545fa69ac26f271e9f86c9b014673dcab62348963253b05e759f2`  
		Last Modified: Fri, 01 Dec 2023 00:14:39 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5f0638945c5b70195a153719380c23d7f5e2811664a885b51a966a2e588491`  
		Last Modified: Fri, 01 Dec 2023 00:14:39 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf83f17dd639cf9b12a89db6bd4fb627135399e4dc76b4c53d5378326d7dcba`  
		Last Modified: Fri, 01 Dec 2023 00:14:42 GMT  
		Size: 87.1 MB (87118384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f9991116413f0fd9400a7fc58c192cebfbf46ed8f145ae8802857f4377bbcc`  
		Last Modified: Fri, 01 Dec 2023 00:14:39 GMT  
		Size: 8.7 KB (8684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bade5106a8a873baf1d457f396aeb25ce98844f926b5aa9dd3f6e14a1bc79eb8`  
		Last Modified: Fri, 01 Dec 2023 00:14:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f994c4ac63efb3feca950de9fbd599456d772ad295d45ec62b8e60c8eaab61f`  
		Last Modified: Fri, 01 Dec 2023 00:14:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a93f38c74b6f37f766f4be89d3888d65ef5206bfe997fbcbd2fe0c40d794f6`  
		Last Modified: Fri, 01 Dec 2023 00:14:41 GMT  
		Size: 4.8 KB (4783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:6ebcbb61051c7920cd1d1ea1dc19323536dde24232a8a939b9c0af6e742f800d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.0 KB (840989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939b848bb6743002970a81262893584e773544dd7572ca27707b884c53dd6cea`

```dockerfile
```

-	Layers:
	-	`sha256:653dcc5f69a20c90f67d27a4972dbea127650a658d31079c464270811254592b`  
		Last Modified: Fri, 01 Dec 2023 00:14:40 GMT  
		Size: 805.3 KB (805273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e229da7b0c7a331af7acc7ff47b38f134401c23dff84c65d7615288f8f32bb5c`  
		Last Modified: Fri, 01 Dec 2023 00:14:39 GMT  
		Size: 35.7 KB (35716 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.18` - linux; arm variant v6

```console
$ docker pull postgres@sha256:8ab7ab6f77801b3710f1c9586dc9e02b4b64bb9c10f9767deebb12dc1fee4ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91488861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc23cf3ff08c42f5544f8875d979a4493f8df92c9fb7c38929e79e5c9027fc56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 19:16:09 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 19:16:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PG_MAJOR=12
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PG_VERSION=12.17
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PG_SHA256=93e8e1b23981d5f03c6c5763f77b28184c1ce4db7194fa466e2edb65d9c1c5f6
# Thu, 09 Nov 2023 19:16:09 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 Nov 2023 19:16:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"12.17","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@12.17?os_name=alpine&os_version=3.18"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 19:16:09 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 19:16:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 19:16:09 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 19:16:09 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 19:16:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d85e8a1148e7602b0b44182dc8fa4c488db0b2e5ecd52e50022dbc19307fcf3`  
		Last Modified: Tue, 14 Nov 2023 01:25:29 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1e0d941bbfc194bc696cd55fc73d21834b0b4f8b19dae1baec3f8ce2550f11`  
		Last Modified: Tue, 14 Nov 2023 01:25:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9195f6de05a86fdae231f631b2442834502e0e3d3f195990a7a48d4ee07c32`  
		Last Modified: Tue, 14 Nov 2023 02:57:41 GMT  
		Size: 88.3 MB (88328419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d289cbe6d1f134b31cd50c037d249656a469e02b18614203d8bfe4089bdd662b`  
		Last Modified: Tue, 14 Nov 2023 02:57:28 GMT  
		Size: 8.7 KB (8690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb99cda33c90f8fe010e9a6796b07a033e34c4a46e3a681e845611560438bcd`  
		Last Modified: Tue, 14 Nov 2023 02:57:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2e1aa00e9033295dc3dfcb252f9bf5b35a579e6b94a035869b17a8ebc7dc17`  
		Last Modified: Tue, 14 Nov 2023 02:57:28 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ceae82ff5d53cad7a174bddbbecb59de07e0d61100fba3bef78f8d5d852bb4`  
		Last Modified: Tue, 14 Nov 2023 02:57:29 GMT  
		Size: 4.8 KB (4785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine3.18` - linux; arm variant v7

```console
$ docker pull postgres@sha256:5374e79d71d11a9b1f3965068a2cfe36b850872b4f77f9c7211140bd9d151b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86091660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baee8a452b78aba879a5f692d27c589aed6ee579502d84e7d762a9cf18761be2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 19:16:09 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 19:16:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PG_MAJOR=12
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PG_VERSION=12.17
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PG_SHA256=93e8e1b23981d5f03c6c5763f77b28184c1ce4db7194fa466e2edb65d9c1c5f6
# Thu, 09 Nov 2023 19:16:09 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 Nov 2023 19:16:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"12.17","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@12.17?os_name=alpine&os_version=3.18"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 19:16:09 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 19:16:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 19:16:09 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 19:16:09 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 19:16:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de34561774cc0a52beeb06fef6a1f6af2bd2a08d4ea304d8d6da8fca56b666f`  
		Last Modified: Fri, 29 Sep 2023 17:52:13 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f40d1b3c22c63e3341b41845b4002cf47594b6e022558becb3c12725dbea465`  
		Last Modified: Fri, 29 Sep 2023 17:52:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266835d8c425f54a2f078ecf30bcedae0f8fe87013a2b164666047b2f9ed0032`  
		Last Modified: Tue, 14 Nov 2023 04:57:39 GMT  
		Size: 83.2 MB (83176609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb37b5b683d95c80c11b92fdd737008702c175c1d10c8a6dfe76a7cd7ebf10e`  
		Last Modified: Tue, 14 Nov 2023 04:57:36 GMT  
		Size: 8.7 KB (8686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624fb83de9a608d32878c2835dfafa8e5741326166aaaec45823b8eb2887641c`  
		Last Modified: Tue, 14 Nov 2023 04:57:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e71b2f9b269c5e1ca3a51299028e638ecb40ba098dba4e3f5eb5339b3eee6e6`  
		Last Modified: Tue, 14 Nov 2023 04:57:36 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ed1a72efdfce0599e090e652f42319007735cb9a2607121a2b8884196d8a13`  
		Last Modified: Tue, 14 Nov 2023 04:57:37 GMT  
		Size: 4.8 KB (4784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:fb9c21400812877958d996a512b24b2ecfc4d14149ff0ada4808cd553e4989b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.9 KB (841862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5473b0a276175409190b1ffd797b6d9e3bd8db13bbbb8555bee30d7d98327065`

```dockerfile
```

-	Layers:
	-	`sha256:53dd7ee77045fcabcc7ef0c15649f7d9a9946672dc9763541051c5ba8ea6f522`  
		Last Modified: Tue, 14 Nov 2023 04:57:36 GMT  
		Size: 806.2 KB (806176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d43197ef578977c6732bc142e61de74c90fa75d27dec6637bc7df6d989f92803`  
		Last Modified: Tue, 14 Nov 2023 04:57:36 GMT  
		Size: 35.7 KB (35686 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:11e3ac4b718feb159f04b19169266da0dfeaa72addbddfbfe19a2ed3c980e55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91933188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68626aff1072e30462ec343794a8772479abd6e8ca5e0bad4b541694bb452e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 19:16:09 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 19:16:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PG_MAJOR=12
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PG_VERSION=12.17
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PG_SHA256=93e8e1b23981d5f03c6c5763f77b28184c1ce4db7194fa466e2edb65d9c1c5f6
# Thu, 09 Nov 2023 19:16:09 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 Nov 2023 19:16:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"12.17","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@12.17?os_name=alpine&os_version=3.18"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 19:16:09 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 19:16:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 19:16:09 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 19:16:09 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 19:16:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57128d869f4112bd058a44bc2fd19d9b05ea0895b34ad51c07e45ddadd30d480`  
		Last Modified: Fri, 29 Sep 2023 17:14:32 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1755e5b66878a2e0b911de75610a642179f0862fd67d7ac96105919310c7ee6`  
		Last Modified: Fri, 29 Sep 2023 17:14:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6515402a6daf2d6e50fd6ab7df6762cb40c1a3be9a7e0e0ebbfe1837e6429861`  
		Last Modified: Tue, 14 Nov 2023 02:23:25 GMT  
		Size: 88.6 MB (88586214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cca12d35877921ff78cbf7794b8bb0a24966736cd77825e5d8cd9b08d66d4a`  
		Last Modified: Tue, 14 Nov 2023 02:23:23 GMT  
		Size: 8.7 KB (8685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea19077111f337646d85a62f2fcd8262f72d681b24b43b2166504a609d9a372`  
		Last Modified: Tue, 14 Nov 2023 02:23:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb749e45432dc08b4a0364da612deaa0e7be8884be43acccd4aee58d111705a`  
		Last Modified: Tue, 14 Nov 2023 02:23:23 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223a93fa6db85d2ed4915ba2a31ad4d32d67cdd750fc3c72adc6fcf5c3b186dc`  
		Last Modified: Tue, 14 Nov 2023 02:23:24 GMT  
		Size: 4.8 KB (4784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:6b63a0a6bff483948b5ec173969575db380ab43b0663a8267dfe5c7d2b2317fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.7 KB (841712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b6c7b26d8f880ab2c0d6a3c9918e57d76cd2f1b63b6a6b256f96cc1d77fd7e`

```dockerfile
```

-	Layers:
	-	`sha256:772df7e00eec938e10d29d904a7ea854cdc085eafdc87accf6a60dbe6460503b`  
		Last Modified: Tue, 14 Nov 2023 02:23:23 GMT  
		Size: 806.2 KB (806151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a91af4dee43033ddeb95093426378479b3e7d32ffbe85878a0f2f1fa2d37ef1`  
		Last Modified: Tue, 14 Nov 2023 02:23:23 GMT  
		Size: 35.6 KB (35561 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.18` - linux; 386

```console
$ docker pull postgres@sha256:a0741d40d5bd742f05597ba999dd71f45793cf23670ff879f9e936934b18f5d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95852348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f56cb02f523fa2ed59ede90b45aeb69205e6c4ff0ed6b737ee966e6ed808a31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 28 Sep 2023 20:38:19 GMT
ADD file:8402753f294e403e92353bd65c86a6428c960be5116c0a15484b663a84f66fcd in / 
# Thu, 28 Sep 2023 20:38:20 GMT
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
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"12.16","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@12.16?os_name=alpine&os_version=3.18"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
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
	-	`sha256:dc95107ad2a031a015320bb397f73ec151d738127175b31ad643120697dc7e90`  
		Last Modified: Thu, 28 Sep 2023 20:39:32 GMT  
		Size: 3.2 MB (3235757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2361d49d5e884bc356dc3a99780fe07508c517deea56eb189574ffb4e7a2dade`  
		Last Modified: Tue, 17 Oct 2023 19:05:33 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a068e763669a8f750c7e4e490bc08e5cfcafee3ceeec1268c441caed8de1e3ad`  
		Last Modified: Tue, 17 Oct 2023 19:05:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554c4cd7cd23d123a40f9dd10c22e960299c7f0507ef58453bff2785be2187f0`  
		Last Modified: Tue, 17 Oct 2023 19:05:38 GMT  
		Size: 92.6 MB (92601447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441829c9b7489c20cc0825871f33f9d008947d7954392bd93c836325b5480c2a`  
		Last Modified: Tue, 17 Oct 2023 19:05:33 GMT  
		Size: 8.7 KB (8684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d9074f632e5552f352817fac358e7c54206f7fa917912b98605ce1a669b099`  
		Last Modified: Tue, 17 Oct 2023 19:05:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a937045b7db8d22d91233136b94cfe8db300f1492e5db8bcad97f0f932137e`  
		Last Modified: Tue, 17 Oct 2023 19:05:34 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d213c435b802ae62e5d7c8bb68c30846d2222660d605021a8d4683bb076da4`  
		Last Modified: Tue, 17 Oct 2023 19:05:34 GMT  
		Size: 4.8 KB (4783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:8084b81b32adbcd79ee069c00f2696eb1d13e0a060422aae3e4860fb8780c79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 KB (35463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da24b46e49e553fe5181fc450989a6c2725ee9a3c6cbd2f0185448c33fad0fd0`

```dockerfile
```

-	Layers:
	-	`sha256:c470ab2df006d2edea58da160d6a535ed0b656a0b38cd130205aeb6b44906eb5`  
		Last Modified: Tue, 17 Oct 2023 19:05:33 GMT  
		Size: 35.5 KB (35463 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.18` - linux; ppc64le

```console
$ docker pull postgres@sha256:599fb08e9cd55c922023c2630baaa4f2c9c1e46f8273710cf87b467df86a2c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98397282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a6fda1d8390b9a0cf8c0a3512079a5c42dc072ab991a3abe069a8cdc616746`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 28 Sep 2023 21:22:20 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Thu, 28 Sep 2023 21:22:21 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 19:16:09 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 19:16:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PG_MAJOR=12
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PG_VERSION=12.17
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PG_SHA256=93e8e1b23981d5f03c6c5763f77b28184c1ce4db7194fa466e2edb65d9c1c5f6
# Thu, 09 Nov 2023 19:16:09 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 Nov 2023 19:16:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"12.17","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@12.17?os_name=alpine&os_version=3.18"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 19:16:09 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 19:16:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 19:16:09 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 19:16:09 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 19:16:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0eda61a2703e25325ea1e358d3a74fe87529df79e6beb419567f1bdbbb63df`  
		Last Modified: Fri, 29 Sep 2023 17:20:30 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b29b4ecd4028475762890da3e105d2ad2bb7690a0bff52c89c3d7180aca779`  
		Last Modified: Fri, 29 Sep 2023 17:20:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a001aca2ef84788216b737d3decd47243215c532cc57d5182641d17e783059`  
		Last Modified: Tue, 14 Nov 2023 02:47:26 GMT  
		Size: 95.0 MB (95035624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49da7a0ea9cc9b5137075d302af020865c3c02507b3681eadd3f24e5eec3b591`  
		Last Modified: Tue, 14 Nov 2023 02:47:23 GMT  
		Size: 8.7 KB (8687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1089ed57a52c9470c387cd184b45a60f1674658ec573c46a4cfd15f299b263e`  
		Last Modified: Tue, 14 Nov 2023 02:47:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080ef871b1a38411d25516db6f0ce526db03de8c4497b248dbcb9b40c4ab936e`  
		Last Modified: Tue, 14 Nov 2023 02:47:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac78169ef5185588e5a98920bdb74528680324282ecfa8c35e4ff05554af44b`  
		Last Modified: Tue, 14 Nov 2023 02:47:24 GMT  
		Size: 4.8 KB (4785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:c4a01c486e950cab7eeef60240f012d3b31cb32db829f85f93889601f6ebf79d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.7 KB (838722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266473e5501a3bd89aa576ff735b931f9d2f070c4af66c8b464100f9767b0d07`

```dockerfile
```

-	Layers:
	-	`sha256:8f0429bcf719375f66d7436a117d3ae6e97753a5d9b074c6f2c160a217a25684`  
		Last Modified: Tue, 14 Nov 2023 02:47:23 GMT  
		Size: 803.1 KB (803123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e8ac062b40239d5df7e4baf0f6c7186129dafeed260bddba866f294bfd3fdde`  
		Last Modified: Tue, 14 Nov 2023 02:47:23 GMT  
		Size: 35.6 KB (35599 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.18` - linux; s390x

```console
$ docker pull postgres@sha256:5d0250a2045b6d197a9920cc53df2707eeec27748ea35c9f173a015e32426ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94325730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090b8ba8f9b797c3840a5d9e0d7da3aed49b9fb4e778b61e2d58896807231b71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 19:16:09 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 19:16:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PG_MAJOR=12
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PG_VERSION=12.17
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PG_SHA256=93e8e1b23981d5f03c6c5763f77b28184c1ce4db7194fa466e2edb65d9c1c5f6
# Thu, 09 Nov 2023 19:16:09 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 Nov 2023 19:16:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"12.17","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@12.17?os_name=alpine&os_version=3.18"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 19:16:09 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 19:16:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 19:16:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 19:16:09 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 19:16:09 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 19:16:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ae232bced3defb4eae7f5affb566ea50f50655d575488965e418a8da86b3ed`  
		Last Modified: Fri, 29 Sep 2023 18:03:31 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68a6f64e487e2750fccb626c86600fd10e0346eabb9bdb31da4b7824cac4a0b`  
		Last Modified: Fri, 29 Sep 2023 18:03:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866a88c441ce42954da94b3000525918afc8e96d91aa50d181082c696bf54524`  
		Last Modified: Tue, 14 Nov 2023 02:13:20 GMT  
		Size: 91.1 MB (91095480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d069de2e646c5a2475f6f50bbd2cfe2a2ed8df6cb1461969bd05d2870b3efa3`  
		Last Modified: Tue, 14 Nov 2023 02:13:18 GMT  
		Size: 8.7 KB (8686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3231e8801753325c24bfc8b89447b660247b77750ccbb0fa46d1451e1a6ea81`  
		Last Modified: Tue, 14 Nov 2023 02:13:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb061cafacc079645a2a2dcb7b8edea4b86c718e5354d5c75fcae929a9972be`  
		Last Modified: Tue, 14 Nov 2023 02:13:18 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f5cecaba1c79c5065ee4ef214666065b5764da11d1b9808f06274b5c63f678`  
		Last Modified: Tue, 14 Nov 2023 02:13:18 GMT  
		Size: 4.8 KB (4783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:a5065b650c141785ea1da175062cd8d09582062d0327c49981ee53648a29f571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.1 KB (840055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879043f0accb134c4b098c38626085afda1364ef4c5671501c02514368a55c94`

```dockerfile
```

-	Layers:
	-	`sha256:c57016772bef945f0c2b53eac52897e7b357cdbe04350ce4569efc2a1d5d61a4`  
		Last Modified: Tue, 14 Nov 2023 02:13:18 GMT  
		Size: 804.5 KB (804504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28f91498325d135c8bec090352e902dc3885af8a3cd58a76f8591545b564cc2a`  
		Last Modified: Tue, 14 Nov 2023 02:13:18 GMT  
		Size: 35.6 KB (35551 bytes)  
		MIME: application/vnd.in-toto+json
