## `postgres:15-alpine3.17`

```console
$ docker pull postgres@sha256:2929961220048bbbaa6b9885c707dda6bc635444de077fcfb4afab6d49c657b7
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

### `postgres:15-alpine3.17` - linux; amd64

```console
$ docker pull postgres@sha256:1b78237f706261e1fcd46e3b6979c4bbf547122e2957a5e2a65519724737807d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96228305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dcce7ffd3db34edd8635ac678aca5c532fd4368d8d4441d74f7b5d956c5e649`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Wed, 04 Oct 2023 14:54:45 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
ENV LANG=en_US.utf8
# Wed, 04 Oct 2023 14:54:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_MAJOR=15
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_VERSION=15.4
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_SHA256=baec5a4bdc4437336653b6cb5d9ed89be5bd5c0c58b94e0becee0a999e63c8f9
# Wed, 04 Oct 2023 14:54:45 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 04 Oct 2023 14:54:45 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"15.4","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@15.4?os_name=alpine&os_version=3.17"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
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
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeba0ca554790e7af5102e5e5e5501583b36973ad1329cf766b75b7219b8bd78`  
		Last Modified: Fri, 06 Oct 2023 01:04:33 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abdb587df2104ba900c2ba5aaa71d8964cb6e594be55c5453e87923f551849a`  
		Last Modified: Fri, 06 Oct 2023 01:04:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38972dd07a7a14c2749dfae6cee350c598a3d606362dbc744182b82ecf03289`  
		Last Modified: Fri, 06 Oct 2023 01:04:38 GMT  
		Size: 92.8 MB (92833795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07597b141e9d6d7319de66a131ad1cb75d33059fd61bca06440265a77409a8ec`  
		Last Modified: Fri, 06 Oct 2023 01:04:34 GMT  
		Size: 9.4 KB (9443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3513918baeeba6a1e3f532c6dee2e2d98d8ccc643e51e509dfb5e992cd6782ea`  
		Last Modified: Fri, 06 Oct 2023 01:04:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f3a41b641c0e446c6b37de90a82e80df7ffbfb783dd3093f77040faa2dd8e9`  
		Last Modified: Fri, 06 Oct 2023 01:04:35 GMT  
		Size: 163.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ed605fde6b7053d96092afaba61f9e8c4b8c6f5fb534f6b0f5a7865e7978ce`  
		Last Modified: Fri, 06 Oct 2023 01:04:35 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:84acbb094693b8ae3e02a5c221aa0b71c05eccdbdc4052ae5f213274721e9834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **872.1 KB (872116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2cd8199bcb34e8b2fd0073b1f7f6a2fb0c62d58dea57602184f52f095e053e`

```dockerfile
```

-	Layers:
	-	`sha256:bcc60c0161d25a58efa5563c9a09cb98ccebcf96ffdff4bbcec6334657032bf6`  
		Last Modified: Fri, 06 Oct 2023 01:04:34 GMT  
		Size: 836.4 KB (836429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1c1938ea667097e3c218fea77574e60b9a28d078b7c3963047b03979fe10cd0`  
		Last Modified: Fri, 06 Oct 2023 01:04:33 GMT  
		Size: 35.7 KB (35687 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.17` - linux; arm variant v6

```console
$ docker pull postgres@sha256:fc9a0ff8bb6d8cf80a90b120971a1d68fb81e130e421b6281ee7602b14a976b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93674932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7efbf5441d01339e8be6cb3f0602bcb095a75e66ed94651127d4b0154c0ccc`
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
ENV PG_MAJOR=15
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_VERSION=15.4
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_SHA256=baec5a4bdc4437336653b6cb5d9ed89be5bd5c0c58b94e0becee0a999e63c8f9
# Wed, 04 Oct 2023 14:54:45 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 04 Oct 2023 14:54:45 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"15.4","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@15.4?os_name=alpine&os_version=3.17"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
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
	-	`sha256:edb4880233416f6d3d02e14bc11163d34d5ae14cf0b0133d79e54ac424b6cec5`  
		Last Modified: Fri, 06 Oct 2023 01:19:11 GMT  
		Size: 90.5 MB (90546581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d175e5e80f8c9b2f19ea8978b06e71336842747c4daf92fc4e30da0a60c682`  
		Last Modified: Fri, 06 Oct 2023 01:18:57 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c8ca78423695d2d7a4fda3075a9c72122efc172763cdb7fc5c000235e9c10b`  
		Last Modified: Fri, 06 Oct 2023 01:18:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e966cf85b5ce3cb46837fb122f8b17cd326fdde907f22beaa3662a8255387864`  
		Last Modified: Fri, 06 Oct 2023 01:18:57 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c7d0132fa699a88638b9991659292130a2a69066223c7035441571a169966a`  
		Last Modified: Fri, 06 Oct 2023 01:18:58 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-alpine3.17` - linux; arm variant v7

```console
$ docker pull postgres@sha256:d2a4a45f10cd5ccf34adb302e06d4ebf0dffd749f150985938f611aff7d044dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88210936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172a3a0155ebd85bf5fa2e3a5b6ca8f87dc8a25b3c6949088700d369ce7c2a37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:29 GMT
ADD file:7f36c30ba2b714d09a8650dba1545abdf892443dadbe9113b9a166b84ba7ac3f in / 
# Mon, 07 Aug 2023 19:57:29 GMT
CMD ["/bin/sh"]
# Thu, 10 Aug 2023 18:46:34 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:46:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
ENV PG_MAJOR=15
# Thu, 10 Aug 2023 18:46:34 GMT
ENV PG_VERSION=15.4
# Thu, 10 Aug 2023 18:46:34 GMT
ENV PG_SHA256=baec5a4bdc4437336653b6cb5d9ed89be5bd5c0c58b94e0becee0a999e63c8f9
# Thu, 10 Aug 2023 18:46:34 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 10 Aug 2023 18:46:34 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:46:34 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:46:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:46:34 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:46:34 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:46:34 GMT
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
	-	`sha256:914e0de288f6ed982d3da152c76ea8b8b09594aa7c5bd8e7ffc59cb10b48de56`  
		Last Modified: Fri, 29 Sep 2023 18:48:57 GMT  
		Size: 85.3 MB (85325599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c702c1a8ebd6ea74176422c942111d7cc3b0db3853f02c73fd4fc0ae5d731e4b`  
		Last Modified: Fri, 29 Sep 2023 18:48:53 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27114cad34886ec0e5eb88ba037ff609d5169249678722036c572310d3138eb4`  
		Last Modified: Fri, 29 Sep 2023 18:48:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8fdcd1f2d5b4d413b326fa382f666012c0620886a2be322dd54b80bcd14ea`  
		Last Modified: Fri, 29 Sep 2023 18:48:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c938361686125f8cb52e5384801025d7a7f244ae9af6cee67c4239dd3300eb`  
		Last Modified: Fri, 29 Sep 2023 18:48:54 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:22d375c5646e1a1689c10e147a9d1e6d70af8f2bcaeedfc6ae67a27995afcddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **870.0 KB (869988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa187ca340bb807ff469a0d8935dabb4847940c78ce05a7186621ac77dd2a592`

```dockerfile
```

-	Layers:
	-	`sha256:3f21d93f7c9613a3a2921f3d2b00901cdb17983002065928b1010a44c1314d3a`  
		Last Modified: Fri, 29 Sep 2023 18:48:53 GMT  
		Size: 835.4 KB (835388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbe4d984480cea8c6f5f46b586fb21649244d0bc9d0de97c37f0e5a3d3bfd436`  
		Last Modified: Fri, 29 Sep 2023 18:48:52 GMT  
		Size: 34.6 KB (34600 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:306bbc11d3a649116c264c35d73fe8deb7e997a80283ce19ebe658cfe60ad6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93816508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d910da051870a92940baa2c8dd62ae3c5afbbcb83ddd2adab98beec949075b74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Thu, 10 Aug 2023 18:46:34 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:46:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
ENV PG_MAJOR=15
# Thu, 10 Aug 2023 18:46:34 GMT
ENV PG_VERSION=15.4
# Thu, 10 Aug 2023 18:46:34 GMT
ENV PG_SHA256=baec5a4bdc4437336653b6cb5d9ed89be5bd5c0c58b94e0becee0a999e63c8f9
# Thu, 10 Aug 2023 18:46:34 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 10 Aug 2023 18:46:34 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:46:34 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:46:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:46:34 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:46:34 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:46:34 GMT
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
	-	`sha256:6d0ae120c51fe08f27f509181701c9f4d26397fc0f31198048f7da06d72a55fd`  
		Last Modified: Fri, 29 Sep 2023 17:24:17 GMT  
		Size: 90.5 MB (90542314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3bcb57166f8a5a06d5390f32af138bfe22d36d87ea54c7c726513874b4bfa0`  
		Last Modified: Fri, 29 Sep 2023 17:24:12 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1269b59ea5f522e04379a4568960eea73869f447f0c4f2873d3c6b5655ffd1`  
		Last Modified: Fri, 29 Sep 2023 17:24:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efdd25c5b5bb468ff3ec601f947df6a5eafc1bd308cf6e6ed23e05cec0db119`  
		Last Modified: Fri, 29 Sep 2023 17:24:12 GMT  
		Size: 162.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118da32553d96481eea9a8bd31ba5b08bfb7e4375b8e27bae843258a8f94096e`  
		Last Modified: Fri, 29 Sep 2023 17:24:13 GMT  
		Size: 4.8 KB (4788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:a30e98409c617338f6d668465fe2e6790f5f0f7fb569ad399f902514524a3b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **869.9 KB (869867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a957a32fad93cf04d90738cb7086757ace803fef849b394550fcad37a881b4d`

```dockerfile
```

-	Layers:
	-	`sha256:07a9c2c0096ec140d30ae98a864e1f2914462b5e5a736c45ec135faa7abcd030`  
		Last Modified: Fri, 29 Sep 2023 17:24:12 GMT  
		Size: 835.4 KB (835379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c220dddc3d9188e9e584eb14ec3a60bd47e9e23c517269449bb42f41fe523e5`  
		Last Modified: Fri, 29 Sep 2023 17:24:12 GMT  
		Size: 34.5 KB (34488 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.17` - linux; 386

```console
$ docker pull postgres@sha256:ed11cc81677ecda448aff27af32be5419774062f1b17b6b0f6d356952cdf1894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101096349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43a827c4f44f720ac7c872394ca24bfafcee4741e545573804d512f319b6913`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:30 GMT
ADD file:437e2411fa3e4795a759f54507f41caa000169f0c32600ec49b4397313cd0884 in / 
# Mon, 07 Aug 2023 19:38:30 GMT
CMD ["/bin/sh"]
# Wed, 04 Oct 2023 14:54:45 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
ENV LANG=en_US.utf8
# Wed, 04 Oct 2023 14:54:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_MAJOR=15
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_VERSION=15.4
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_SHA256=baec5a4bdc4437336653b6cb5d9ed89be5bd5c0c58b94e0becee0a999e63c8f9
# Wed, 04 Oct 2023 14:54:45 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 04 Oct 2023 14:54:45 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"15.4","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@15.4?os_name=alpine&os_version=3.17"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
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
	-	`sha256:ddc7d64c528fabaad61cc880e91abba829973f743d753415145211971f9ee10d`  
		Last Modified: Mon, 07 Aug 2023 19:39:10 GMT  
		Size: 3.4 MB (3413779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ba2f82d2f2155f012c1215840d5cb3cd3c0a253b781565df45858c0955dc36`  
		Last Modified: Fri, 06 Oct 2023 01:05:56 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b09cb4e2d1a4b163802eb10c333de763b1e09cd5d911c7c7dfa43ea538b672d`  
		Last Modified: Fri, 06 Oct 2023 01:03:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023a421c3a6f296d8f35de27d44d6f02ff97ba3409f0da59337ff1c74d292b32`  
		Last Modified: Fri, 06 Oct 2023 01:06:04 GMT  
		Size: 97.7 MB (97666674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a8b2cbc697d70985cc08f3d0256e404af1cad4390e2409fa8bf28a125a356f`  
		Last Modified: Fri, 06 Oct 2023 01:05:56 GMT  
		Size: 9.4 KB (9443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c488af03a494dc4a0f69e48714fb343f252e90ebff6b39a1488bd15e024b8`  
		Last Modified: Fri, 06 Oct 2023 01:05:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7422e42b15999e6ec272d21fb39a30620fcad0d00bfa5c3505580c5b1e2ced0`  
		Last Modified: Fri, 06 Oct 2023 01:05:57 GMT  
		Size: 163.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f91ab26a68fbb58c584c3aacc7db8e297f8961ab3532eb6523c9af9eaedd41`  
		Last Modified: Fri, 06 Oct 2023 01:05:57 GMT  
		Size: 4.8 KB (4782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:bb3582a7cceace90404d1ef49ae3800c67b2bd508274b67616d7d905ff313b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 KB (35443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:151b4b774a78c7fb4c236488218edef252bc317c7a050c5c8d4cdcc8fc45c7ce`

```dockerfile
```

-	Layers:
	-	`sha256:59e21b635ee11bcc633cb9ee09f7f0e7ccd9d11a92210d552f2badbbda753f3f`  
		Last Modified: Fri, 06 Oct 2023 01:05:56 GMT  
		Size: 35.4 KB (35443 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.17` - linux; ppc64le

```console
$ docker pull postgres@sha256:d07492cb9a00b131ef397d00d6f16614dc565d9b16924697f689734d8ebe1006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102032064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739b3a72a6436013387571f179fecedb7669f51880375ccb95de30daa94b7423`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:35 GMT
ADD file:52f28bcdd6e1c6f85b2b5d66ace37ed6cef0da8ce5c58e246549427361b64c1d in / 
# Mon, 07 Aug 2023 20:16:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Aug 2023 18:46:34 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:46:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
ENV PG_MAJOR=15
# Thu, 10 Aug 2023 18:46:34 GMT
ENV PG_VERSION=15.4
# Thu, 10 Aug 2023 18:46:34 GMT
ENV PG_SHA256=baec5a4bdc4437336653b6cb5d9ed89be5bd5c0c58b94e0becee0a999e63c8f9
# Thu, 10 Aug 2023 18:46:34 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 10 Aug 2023 18:46:34 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:46:34 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:46:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:46:34 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:46:34 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:46:34 GMT
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
	-	`sha256:d2023aeb249a6ff9a7ba4e0c5c7207e4cd9a81028e682220a3468f2c6454cc04`  
		Last Modified: Fri, 29 Sep 2023 17:38:55 GMT  
		Size: 98.6 MB (98624798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1533b281971fcc6c88e70ccd3d7ca087a8e4d9a051b2fb0508cf20fc5ba1c4f`  
		Last Modified: Fri, 29 Sep 2023 17:38:50 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89206d74fdbb72e638fd56354272a0d8c8a6333b4b6f8828b18c93bb37ded0a7`  
		Last Modified: Fri, 29 Sep 2023 17:38:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08735475414ba8d7ceb8f903de6f9bf70ff8e6e53b4aadf9bbdec15f08dbe39`  
		Last Modified: Fri, 29 Sep 2023 17:38:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acb2729f489f5c9ff03e1dabb004a7585e8d1b523261cfde4f6cf1f29c97d13`  
		Last Modified: Fri, 29 Sep 2023 17:38:51 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:077d0ad9b35853191a6018b3b5d79fb32c47628dc1dde793a1981e329b338ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.5 KB (866481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a21660992233b46f5213b7a459e86c02c4d3774f8af6ffc019fe738f9f6985e`

```dockerfile
```

-	Layers:
	-	`sha256:55725d10e88af9f7e3e4d641e0d1df76ad8f90f8a381eb3fbfb2e2fe4f369e64`  
		Last Modified: Fri, 29 Sep 2023 17:38:50 GMT  
		Size: 832.0 KB (831963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c483f0c450ae0d8e59757a1cb1e4db1d5cd63e1cdacbc7d92665de5202f4fbc`  
		Last Modified: Fri, 29 Sep 2023 17:38:50 GMT  
		Size: 34.5 KB (34518 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.17` - linux; s390x

```console
$ docker pull postgres@sha256:e6d9fb83496fa2545c5eada001176f2401dc51d64081f63ab38ad6081ae7d759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96539473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208b8828764adcb6e09730cbd8d77c728a52c3fb660811144fa142c7c2cd4130`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:42:01 GMT
ADD file:2e221805acb91c51e7afa6b926252ab2260cdf2e166f3d917a98384f3a157622 in / 
# Mon, 07 Aug 2023 19:42:02 GMT
CMD ["/bin/sh"]
# Thu, 10 Aug 2023 18:46:34 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:46:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
ENV PG_MAJOR=15
# Thu, 10 Aug 2023 18:46:34 GMT
ENV PG_VERSION=15.4
# Thu, 10 Aug 2023 18:46:34 GMT
ENV PG_SHA256=baec5a4bdc4437336653b6cb5d9ed89be5bd5c0c58b94e0becee0a999e63c8f9
# Thu, 10 Aug 2023 18:46:34 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 10 Aug 2023 18:46:34 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:46:34 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:46:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:46:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:46:34 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:46:34 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:46:34 GMT
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
	-	`sha256:211e3dbba58bf55f6505740b4d03536039f76ceeb171b872336901d27f84abfc`  
		Last Modified: Fri, 29 Sep 2023 19:28:26 GMT  
		Size: 93.3 MB (93347589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897e26ca43afa928ea3b36c8d808e733ead993f84b960d5fb77e5a59bb9c193b`  
		Last Modified: Fri, 29 Sep 2023 19:28:22 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf4f8a6d985af1f25072d7471943d2c908fdca25c84d9f8e31745555a905d12`  
		Last Modified: Fri, 29 Sep 2023 19:28:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c277fb37d1aa2091f80a785a95648b838eadcdbc03cab88c92a4daa21b33c76`  
		Last Modified: Fri, 29 Sep 2023 19:28:22 GMT  
		Size: 163.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d44184ef5032c0cd37409361add889ceb8fbac74017d5c1835dada51c532bd1`  
		Last Modified: Fri, 29 Sep 2023 19:28:23 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:03746abc649c98655fc06f271b0d0b3b97494c259231a43a762f8ed4fb4bb799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.9 KB (867920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e9309378c0b889688a6bffe9fce4c2af03914566e742469f64750b4eca8c5c`

```dockerfile
```

-	Layers:
	-	`sha256:f0980463af492cb2e8b576ddddc800d81b126c2032e5a2f01089ce4144be2f20`  
		Last Modified: Fri, 29 Sep 2023 19:28:22 GMT  
		Size: 833.4 KB (833438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fcb3628746116d307b079393a3a823638ba5c517e1a1f3a96279b35cae3d665`  
		Last Modified: Fri, 29 Sep 2023 19:28:22 GMT  
		Size: 34.5 KB (34482 bytes)  
		MIME: application/vnd.in-toto+json
