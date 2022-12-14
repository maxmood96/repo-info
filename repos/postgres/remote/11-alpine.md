## `postgres:11-alpine`

```console
$ docker pull postgres@sha256:91ece8e040730b492a84426efe37fd51faeecd5ec37ea0f0b6bbe1d121f9645d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `postgres:11-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:0ebc92ac9141fdffbd5503871b61e37d02e3c479c4e267cb8c0e2015b03e51bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90176506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77c9e9012ffb7bf43dbb18605de6e40626a4dd231aa9fb8d1d039b0219497f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Wed, 30 Nov 2022 22:09:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 30 Nov 2022 22:09:41 GMT
ENV LANG=en_US.utf8
# Wed, 30 Nov 2022 22:09:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 30 Nov 2022 22:20:53 GMT
ENV PG_MAJOR=11
# Wed, 30 Nov 2022 22:20:53 GMT
ENV PG_VERSION=11.18
# Wed, 30 Nov 2022 22:20:53 GMT
ENV PG_SHA256=d24f20efc52e918acfbcca21e9cea28e0e263b846a0c408fcfac3b3c4a0f7504
# Tue, 13 Dec 2022 23:39:26 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		nss_wrapper 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 13 Dec 2022 23:39:27 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 13 Dec 2022 23:39:27 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Dec 2022 23:39:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Dec 2022 23:39:28 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Dec 2022 23:39:28 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Dec 2022 23:39:28 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 13 Dec 2022 23:39:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Dec 2022 23:39:28 GMT
STOPSIGNAL SIGINT
# Tue, 13 Dec 2022 23:39:29 GMT
EXPOSE 5432
# Tue, 13 Dec 2022 23:39:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534a279782786a1033fff3a97ceb57c790d85068dcd05f976c82a4d2b7ba52d0`  
		Last Modified: Wed, 30 Nov 2022 22:24:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d52041f541ee33606ad0644b3fda5d7c29c138ecb3fd12fc7f0c720e448852`  
		Last Modified: Wed, 30 Nov 2022 22:24:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0e0bf8b189128e0541ee3c3bfe88ac8a5836ab75f98fb0c887e7715a123081`  
		Last Modified: Tue, 13 Dec 2022 23:42:22 GMT  
		Size: 86.8 MB (86791311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f108e72c3b40ac835c411399d268f82d501c380178fce6c97670b0ad8a9b5fd`  
		Last Modified: Tue, 13 Dec 2022 23:42:10 GMT  
		Size: 8.0 KB (7992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313b5229af34ad745324a3c741cf58783071d89d7cba193fb99537fa7ead006f`  
		Last Modified: Tue, 13 Dec 2022 23:42:11 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e634ddd1ccfad4d8ac6e635e1dbc9cd41c7d73adb70de3ca0985bf91b6c68a6`  
		Last Modified: Tue, 13 Dec 2022 23:42:11 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcf3645c35e03fd005e9346f72ea896cfba5e67610277f218867bdd2e991410`  
		Last Modified: Tue, 13 Dec 2022 23:42:10 GMT  
		Size: 4.7 KB (4704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:f3852862c8319251170b621e3d572b0278607e78d4687eee6a8c47d91d8b4d48
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88071017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f75a0d80f843c28344cdbb2304bb536c0e2cabec03d5998a1ab88190e1da931`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 22 Nov 2022 22:55:46 GMT
ADD file:132c76d7f7dae2f51f589ee460f1870a2cec6e9dc7ff8e38e88fcee2cfbe70da in / 
# Tue, 22 Nov 2022 22:55:46 GMT
CMD ["/bin/sh"]
# Wed, 30 Nov 2022 21:10:19 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 30 Nov 2022 21:10:19 GMT
ENV LANG=en_US.utf8
# Wed, 30 Nov 2022 21:10:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 30 Nov 2022 21:23:39 GMT
ENV PG_MAJOR=11
# Wed, 30 Nov 2022 21:23:39 GMT
ENV PG_VERSION=11.18
# Wed, 30 Nov 2022 21:23:39 GMT
ENV PG_SHA256=d24f20efc52e918acfbcca21e9cea28e0e263b846a0c408fcfac3b3c4a0f7504
# Tue, 13 Dec 2022 23:28:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		nss_wrapper 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 13 Dec 2022 23:28:27 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 13 Dec 2022 23:28:28 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Dec 2022 23:28:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Dec 2022 23:28:30 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Dec 2022 23:28:30 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Dec 2022 23:28:30 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 13 Dec 2022 23:28:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Dec 2022 23:28:30 GMT
STOPSIGNAL SIGINT
# Tue, 13 Dec 2022 23:28:31 GMT
EXPOSE 5432
# Tue, 13 Dec 2022 23:28:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c2eb4db52fbe1266a78d8c185d33544a2916faa7d82fb5f50909fe233e0579da`  
		Last Modified: Tue, 22 Nov 2022 22:56:39 GMT  
		Size: 3.1 MB (3107138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd022df475c75e388b1fd7a4163f33c0ff1b1d74fdc20b70d7997fe03aa044af`  
		Last Modified: Wed, 30 Nov 2022 21:27:53 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed70ce3a42bb46bc919e74b0e65503324722dcbef23cf71e04c33adf27e1835`  
		Last Modified: Wed, 30 Nov 2022 21:27:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd14c20ce8ff53fe2a3d4eb23d96db880a7be03041757ce4d67c1b19f941b0a`  
		Last Modified: Tue, 13 Dec 2022 23:32:16 GMT  
		Size: 84.9 MB (84949519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce25f5e15a3b401a0f703f2114a9f38add75e69481884c6a96b292906f1be804`  
		Last Modified: Tue, 13 Dec 2022 23:32:02 GMT  
		Size: 8.0 KB (7989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc6bb066c99b04add2d00f479ce76a29ea25eed50a1b28a3f1587504eb101e5`  
		Last Modified: Tue, 13 Dec 2022 23:32:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f04ed082d694cc5e8078515b928688f73751faf1d5269e8468eedf22a204472`  
		Last Modified: Tue, 13 Dec 2022 23:32:02 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f524b9ef1f937c16287046939b14d0ba0dc503316507bc2487604da9372abf01`  
		Last Modified: Tue, 13 Dec 2022 23:32:02 GMT  
		Size: 4.7 KB (4706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:54c01ffc574901f07ba0d3c19a346b8aa227d46ccb4bdd6efe4dbd3b2574ced5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82854081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43c560659fbe5ad9f24ce2fed3e34437850f3cd5ec871410b5979a561fb6012`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 22 Nov 2022 22:57:20 GMT
ADD file:080010d9005e8e0dae3e98c7f9afff3e3a40ed32579ca01946efc6ede8316bad in / 
# Tue, 22 Nov 2022 22:57:20 GMT
CMD ["/bin/sh"]
# Wed, 30 Nov 2022 21:24:31 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 30 Nov 2022 21:24:31 GMT
ENV LANG=en_US.utf8
# Wed, 30 Nov 2022 21:24:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 30 Nov 2022 21:38:06 GMT
ENV PG_MAJOR=11
# Wed, 30 Nov 2022 21:38:06 GMT
ENV PG_VERSION=11.18
# Wed, 30 Nov 2022 21:38:06 GMT
ENV PG_SHA256=d24f20efc52e918acfbcca21e9cea28e0e263b846a0c408fcfac3b3c4a0f7504
# Tue, 13 Dec 2022 23:13:31 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		nss_wrapper 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 13 Dec 2022 23:13:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 13 Dec 2022 23:13:33 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Dec 2022 23:13:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Dec 2022 23:13:35 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Dec 2022 23:13:35 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Dec 2022 23:13:35 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 13 Dec 2022 23:13:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Dec 2022 23:13:35 GMT
STOPSIGNAL SIGINT
# Tue, 13 Dec 2022 23:13:35 GMT
EXPOSE 5432
# Tue, 13 Dec 2022 23:13:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cb2ec849933dd31db64abae3fdcb6923c490d9795577bee1ee1be04eab0376ee`  
		Last Modified: Tue, 22 Nov 2022 22:58:12 GMT  
		Size: 2.9 MB (2865346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ff09f15b2005f6cc7b283cb6b00059ad4d0ac79d1fc45f9cc19812e2204443`  
		Last Modified: Wed, 30 Nov 2022 21:43:00 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1306f705d7bd596b648dce0baffcecc255840db04271a39efba39954d04d82e9`  
		Last Modified: Wed, 30 Nov 2022 21:43:00 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae664a66eae1877a0d9ac5ca283756e986d26b184278ec93423ab7133acb205`  
		Last Modified: Tue, 13 Dec 2022 23:18:21 GMT  
		Size: 80.0 MB (79974376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5414a8a793ce82f847e8c88dc9e8bd1d4996d702c94d66c0db3135dab4f7d4c`  
		Last Modified: Tue, 13 Dec 2022 23:18:10 GMT  
		Size: 8.0 KB (7989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4041880be60eff67facb0bacbda2eb2e7507fb29c43183bec63a80be3d9fc9b`  
		Last Modified: Tue, 13 Dec 2022 23:18:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad6ba5d9f98e470930dadf68280d68b6b46eed254a90b0cc289bf697ab749d7`  
		Last Modified: Tue, 13 Dec 2022 23:18:09 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce0d1635f8e6216c6666462af2af964d6ecae1c22a3933e7f773595526e37ca`  
		Last Modified: Tue, 13 Dec 2022 23:18:09 GMT  
		Size: 4.7 KB (4704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:9ceb8968ed87e296ef478147b8301f82980de69158cca4b8c5d4da9dd4f5ff40
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (87998756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c94b629b5a64da2005944a7622a8381d8e62ae823daab60b03da5e0685a496f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 22 Nov 2022 22:39:21 GMT
ADD file:685b5edadf1d5bf0aeb2aec35f810d83876e6d2ea0903b213f75a9c5f0dc5901 in / 
# Tue, 22 Nov 2022 22:39:21 GMT
CMD ["/bin/sh"]
# Wed, 30 Nov 2022 21:41:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 30 Nov 2022 21:41:48 GMT
ENV LANG=en_US.utf8
# Wed, 30 Nov 2022 21:41:48 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 30 Nov 2022 21:50:14 GMT
ENV PG_MAJOR=11
# Wed, 30 Nov 2022 21:50:14 GMT
ENV PG_VERSION=11.18
# Wed, 30 Nov 2022 21:50:14 GMT
ENV PG_SHA256=d24f20efc52e918acfbcca21e9cea28e0e263b846a0c408fcfac3b3c4a0f7504
# Tue, 13 Dec 2022 23:04:33 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		nss_wrapper 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 13 Dec 2022 23:04:34 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 13 Dec 2022 23:04:34 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Dec 2022 23:04:35 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Dec 2022 23:04:35 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Dec 2022 23:04:35 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Dec 2022 23:04:35 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 13 Dec 2022 23:04:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Dec 2022 23:04:35 GMT
STOPSIGNAL SIGINT
# Tue, 13 Dec 2022 23:04:35 GMT
EXPOSE 5432
# Tue, 13 Dec 2022 23:04:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:261da4162673b93e5c0e7700a3718d40bcc086dbf24b1ec9b54bca0b82300626`  
		Last Modified: Tue, 22 Nov 2022 22:39:45 GMT  
		Size: 3.3 MB (3259190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc5a1575ff6ac91556b51a6d477d71d5e2651299fd7bfb2c544e512dea7ce11`  
		Last Modified: Wed, 30 Nov 2022 21:52:51 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4753903688c57201bee69249a606bbb11e98bf3158068094a6606a05a8b85eaa`  
		Last Modified: Wed, 30 Nov 2022 21:52:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14115702822ad2a1752e59fb069cf77becb3aea84770209e3c4919647de4090`  
		Last Modified: Tue, 13 Dec 2022 23:07:12 GMT  
		Size: 84.7 MB (84725089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd4728f352b2351bb0e2673ef8e5f1b7af5d4d8ed762fbfb533c002ecd22811`  
		Last Modified: Tue, 13 Dec 2022 23:07:04 GMT  
		Size: 8.0 KB (7989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f293c19cccac1fc167484473907a3c9d9313819d9d74a15e80960fdf80f957`  
		Last Modified: Tue, 13 Dec 2022 23:07:04 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe0bd5cbd47de72ebb0de450e56df009c34bc9567c2f97a9683cc4a07648e18`  
		Last Modified: Tue, 13 Dec 2022 23:07:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63489d11f759c0b5d62f428ac060e081acfeec494b04a8e34519bf20132baf1b`  
		Last Modified: Tue, 13 Dec 2022 23:07:04 GMT  
		Size: 4.7 KB (4699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; 386

```console
$ docker pull postgres@sha256:75f061cfa45a939cb9ccd1e155e912fbf8351ca43b11c6337cf7b61a02fed0cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94795651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c2484954341762a438de12a84dd656ef10af4fba99bf004f8edbd16cbad5e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 22 Nov 2022 22:38:24 GMT
ADD file:f2fbc3153694110f7004f005c4e18435b171ed44a3b35498a1b4916ef1e9af43 in / 
# Tue, 22 Nov 2022 22:38:25 GMT
CMD ["/bin/sh"]
# Wed, 30 Nov 2022 20:46:32 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 30 Nov 2022 20:46:33 GMT
ENV LANG=en_US.utf8
# Wed, 30 Nov 2022 20:46:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 30 Nov 2022 20:59:27 GMT
ENV PG_MAJOR=11
# Wed, 30 Nov 2022 20:59:28 GMT
ENV PG_VERSION=11.18
# Wed, 30 Nov 2022 20:59:29 GMT
ENV PG_SHA256=d24f20efc52e918acfbcca21e9cea28e0e263b846a0c408fcfac3b3c4a0f7504
# Tue, 13 Dec 2022 23:18:50 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		nss_wrapper 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 13 Dec 2022 23:18:51 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 13 Dec 2022 23:18:52 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Dec 2022 23:18:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Dec 2022 23:18:54 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Dec 2022 23:18:55 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Dec 2022 23:18:57 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 13 Dec 2022 23:18:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Dec 2022 23:18:58 GMT
STOPSIGNAL SIGINT
# Tue, 13 Dec 2022 23:18:59 GMT
EXPOSE 5432
# Tue, 13 Dec 2022 23:19:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3cc7ae06783159e8c992cfb745833f904e836c74a7704b7a90b4b45a598f878c`  
		Last Modified: Tue, 22 Nov 2022 22:39:08 GMT  
		Size: 3.4 MB (3408493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49a37c442de2a21f08a06c070be942937c1aeb2d575ee7f97481ddb0824cf78`  
		Last Modified: Wed, 30 Nov 2022 21:03:52 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a23eec619e4e811c404de0e825eec062d21d1d543ff1e9c155b84e71aeac772`  
		Last Modified: Wed, 30 Nov 2022 21:03:52 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32887bc2841d5d1ca92c958edb4678fad143e10d6fcc282af9acfda711323d9f`  
		Last Modified: Tue, 13 Dec 2022 23:22:58 GMT  
		Size: 91.4 MB (91372793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470f61d5ab0b1b3c7df80ea67757fb73ccfcde521312fa6a4ff135ff4cd5bcb0`  
		Last Modified: Tue, 13 Dec 2022 23:22:47 GMT  
		Size: 8.0 KB (7985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536b836cef4a2cd8604939073afa0d41880412131125cb941b146dc0d1c6f16e`  
		Last Modified: Tue, 13 Dec 2022 23:22:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f95bc71e4810b8914e195ac725a53fe266daaf2a7ad0f2431a733230d541411`  
		Last Modified: Tue, 13 Dec 2022 23:22:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0d19f87fbac098cec5988d4f2c60bfa85a83f5018dc7f86ccf600e6bfe5842`  
		Last Modified: Tue, 13 Dec 2022 23:22:47 GMT  
		Size: 4.7 KB (4704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:fff15825a7b9e66b3d57e454bda02fb99e9ac6ce82c4ae4b2ea088d1eea1f8f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95796562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb0d2e3cdf48c4050597ada8d189b0c6bdfe058c6982bd500b18c401a21edd6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 23 Nov 2022 00:18:18 GMT
ADD file:a8e68f93c597f70ce637ef578c72c9b41b4b8d80b552b8e5570d4efcc1d02ff5 in / 
# Wed, 23 Nov 2022 00:18:18 GMT
CMD ["/bin/sh"]
# Wed, 30 Nov 2022 22:15:26 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 30 Nov 2022 22:15:26 GMT
ENV LANG=en_US.utf8
# Wed, 30 Nov 2022 22:15:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 30 Nov 2022 22:30:12 GMT
ENV PG_MAJOR=11
# Wed, 30 Nov 2022 22:30:12 GMT
ENV PG_VERSION=11.18
# Wed, 30 Nov 2022 22:30:13 GMT
ENV PG_SHA256=d24f20efc52e918acfbcca21e9cea28e0e263b846a0c408fcfac3b3c4a0f7504
# Wed, 30 Nov 2022 22:33:11 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 30 Nov 2022 22:33:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 30 Nov 2022 22:33:16 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 30 Nov 2022 22:33:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 30 Nov 2022 22:33:18 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 30 Nov 2022 22:33:18 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 30 Nov 2022 22:33:18 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Wed, 30 Nov 2022 22:33:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Nov 2022 22:33:19 GMT
STOPSIGNAL SIGINT
# Wed, 30 Nov 2022 22:33:20 GMT
EXPOSE 5432
# Wed, 30 Nov 2022 22:33:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:69314845b945e4b33e4ee552d0e4156645f71c81b6cb71108c1e32e139aec052`  
		Last Modified: Wed, 23 Nov 2022 00:19:02 GMT  
		Size: 3.4 MB (3384500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc29c399cd4dacf010e87247d4a43106ebbd449f478f37e3a8d01a44ee6a4ea`  
		Last Modified: Wed, 30 Nov 2022 22:35:13 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd7a1770ebbfd68796e4f2f727c79ffce21899bddacdfe0e25aa78c4344ac46`  
		Last Modified: Wed, 30 Nov 2022 22:35:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac685f51c8cca7776f200e3acb369f8073e3337f8708ff4cad14f375dfb7363e`  
		Last Modified: Wed, 30 Nov 2022 22:38:25 GMT  
		Size: 92.4 MB (92397572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f39ad798c7477edf66167394a1ec100472de3988abefd1f6c54073e4c179ba`  
		Last Modified: Wed, 30 Nov 2022 22:38:03 GMT  
		Size: 8.0 KB (7993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b46fb59c21a301c49dcba83c249b8ce8f5c9878808a560d2ed0b2206d3325a1`  
		Last Modified: Wed, 30 Nov 2022 22:38:03 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a76f1b3238de0c2ed2172fb1e9557c6946f2374ad670e91d632bab46ee7befb`  
		Last Modified: Wed, 30 Nov 2022 22:38:03 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00afad5dc00a1078fb1d5b97aaabc23f4e2cc0e08fa1739a62ca8cd9dd8e2e3f`  
		Last Modified: Wed, 30 Nov 2022 22:38:03 GMT  
		Size: 4.7 KB (4706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:0765f8e670bd09cec00e8fbde745e0be6f7df34ebc3741b8384f2b46bd553463
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90652690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ecd9eacb36f18e79d4c0b4036a82cbf3da3b91ce8722377559042322ca12d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 22 Nov 2022 22:47:02 GMT
ADD file:d8cbd162b64e4b7a8b83086be37ef5ee69e955ac955ebbe59e70c6be2a2d1a9f in / 
# Tue, 22 Nov 2022 22:47:03 GMT
CMD ["/bin/sh"]
# Wed, 30 Nov 2022 21:25:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 30 Nov 2022 21:25:41 GMT
ENV LANG=en_US.utf8
# Wed, 30 Nov 2022 21:25:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 30 Nov 2022 21:36:58 GMT
ENV PG_MAJOR=11
# Wed, 30 Nov 2022 21:36:58 GMT
ENV PG_VERSION=11.18
# Wed, 30 Nov 2022 21:36:58 GMT
ENV PG_SHA256=d24f20efc52e918acfbcca21e9cea28e0e263b846a0c408fcfac3b3c4a0f7504
# Tue, 13 Dec 2022 23:32:54 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		nss_wrapper 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 13 Dec 2022 23:33:04 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 13 Dec 2022 23:33:05 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Dec 2022 23:33:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Dec 2022 23:33:07 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Dec 2022 23:33:07 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Dec 2022 23:33:08 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 13 Dec 2022 23:33:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Dec 2022 23:33:08 GMT
STOPSIGNAL SIGINT
# Tue, 13 Dec 2022 23:33:08 GMT
EXPOSE 5432
# Tue, 13 Dec 2022 23:33:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:844b8973ca9523380e35625da9a5fd2d50338c403129146541e13d0722c056f7`  
		Last Modified: Tue, 22 Nov 2022 22:47:59 GMT  
		Size: 3.2 MB (3170814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e278c29da4e88947f0cf508855d1d896131ea7b8ddbe6f306e8314d9a3edab`  
		Last Modified: Wed, 30 Nov 2022 21:41:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5e60a6975908e5003d121a4ff442fc39146ab3c7f7c4e0d9dd52b9814f59c2`  
		Last Modified: Wed, 30 Nov 2022 21:41:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efedc8d67c46bb5bd3ae5aae1a0bbf4a75392b5a8e7e5df25c2de27e4a5ab23`  
		Last Modified: Tue, 13 Dec 2022 23:37:11 GMT  
		Size: 87.5 MB (87467392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da92bcd4365a0022ebc679d5078d26a9c7290753dd58c8e1958218bc790c5aca`  
		Last Modified: Tue, 13 Dec 2022 23:37:01 GMT  
		Size: 8.0 KB (7990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b658f92c7e81b93563ffd2a1bcffb27fbb13907d0dd91344f39503bb12d14594`  
		Last Modified: Tue, 13 Dec 2022 23:37:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30c54553a3a4628c1ab363288a55894023b9f02522a3dc80a768c3d82df55d5`  
		Last Modified: Tue, 13 Dec 2022 23:37:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4493aa6f6d7d4101db7a1f86992db4c9ee6a666122944d0153cca3ad74f34005`  
		Last Modified: Tue, 13 Dec 2022 23:37:01 GMT  
		Size: 4.7 KB (4703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
