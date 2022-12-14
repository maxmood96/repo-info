## `postgres:alpine`

```console
$ docker pull postgres@sha256:e5a7d01f4fa15440f5828265cf24005fc2364c4c42c3ba8a2884dbdeb88526ee
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

### `postgres:alpine` - linux; amd64

```console
$ docker pull postgres@sha256:64e93f7ce6e632ef40e070ff2a4a92c66aa8fe1017fe44dd0545aaa854dd5de6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94091560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac95006e92d16b385d703415bc3bfcecba08dcb35d5ab7c45c143c8421c84592`
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
# Wed, 30 Nov 2022 22:09:41 GMT
ENV PG_MAJOR=15
# Wed, 30 Nov 2022 22:09:41 GMT
ENV PG_VERSION=15.1
# Wed, 30 Nov 2022 22:09:41 GMT
ENV PG_SHA256=64fdf23d734afad0dfe4077daca96ac51dcd697e68ae2d3d4ca6c45cb14e21ae
# Tue, 13 Dec 2022 23:28:31 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		nss_wrapper 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 13 Dec 2022 23:28:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 13 Dec 2022 23:28:33 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Dec 2022 23:28:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Dec 2022 23:28:33 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Dec 2022 23:28:33 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Dec 2022 23:28:34 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 13 Dec 2022 23:28:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Dec 2022 23:28:34 GMT
STOPSIGNAL SIGINT
# Tue, 13 Dec 2022 23:28:34 GMT
EXPOSE 5432
# Tue, 13 Dec 2022 23:28:34 GMT
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
	-	`sha256:2bf42692bedd14f497269cf7ab03000979e85a043a12438d9468295b76d8cf6b`  
		Last Modified: Tue, 13 Dec 2022 23:40:31 GMT  
		Size: 90.7 MB (90704907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f54ae369e8f9937a3febff2af921cd3ecac557dafc2361f4ac7cea68aea498a`  
		Last Modified: Tue, 13 Dec 2022 23:40:20 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad124809424d072dcb43334d53f4858c39be2fd2a177ba7382a125c125f1ab4`  
		Last Modified: Tue, 13 Dec 2022 23:40:20 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765558788e597a4a8011a9bc3c4ff0f8ff3972de4d6349038a777707dc998799`  
		Last Modified: Tue, 13 Dec 2022 23:40:21 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb9784aa7b08d9af3db6c0503b2a1520c9b72ac535b7120a8d71ab5165ba805`  
		Last Modified: Tue, 13 Dec 2022 23:40:20 GMT  
		Size: 4.7 KB (4703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:1b3a06ceb2245978364c097b01b8f4f89723e4ab8e4e5fb0df3686ba264f8957
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91902146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60ea9e0e36fc89af2ad2f7d93639488cadce6b1f33519274e79fa6d8168c935`
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
# Wed, 30 Nov 2022 21:10:20 GMT
ENV PG_MAJOR=15
# Wed, 30 Nov 2022 21:10:20 GMT
ENV PG_VERSION=15.1
# Wed, 30 Nov 2022 21:10:20 GMT
ENV PG_SHA256=64fdf23d734afad0dfe4077daca96ac51dcd697e68ae2d3d4ca6c45cb14e21ae
# Tue, 13 Dec 2022 23:15:05 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		nss_wrapper 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 13 Dec 2022 23:15:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 13 Dec 2022 23:15:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Dec 2022 23:15:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Dec 2022 23:15:07 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Dec 2022 23:15:07 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Dec 2022 23:15:07 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 13 Dec 2022 23:15:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Dec 2022 23:15:07 GMT
STOPSIGNAL SIGINT
# Tue, 13 Dec 2022 23:15:07 GMT
EXPOSE 5432
# Tue, 13 Dec 2022 23:15:07 GMT
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
	-	`sha256:2c4dbda4927e88bb1c48847f5aa3fafa3c31a747c3363e9cc4df171097780b21`  
		Last Modified: Tue, 13 Dec 2022 23:29:56 GMT  
		Size: 88.8 MB (88779189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4aada166cdf20af9eac5e77e20bff003bc328274103efdd912f4a21f0af84d`  
		Last Modified: Tue, 13 Dec 2022 23:29:42 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d49ea290205605d4677d2361145998b15036604da86f7aaeb8be54fcad6c413`  
		Last Modified: Tue, 13 Dec 2022 23:29:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1dbe047cb670af04c18a8f4cde22c4ab25f314c2f07e2e93bb44e27891496e`  
		Last Modified: Tue, 13 Dec 2022 23:29:42 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e653bd82f0ba4f4998dabf5616fac1dc591a8c57289c12840977e5d918751f`  
		Last Modified: Tue, 13 Dec 2022 23:29:42 GMT  
		Size: 4.7 KB (4702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:6e1676a5be96ac680f562bd2313575d879090906efb61c0b318b40128b59ef6f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86526903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fa40087895a1c891cb3200466fb619c2b796306b2137a44aee3c6d78ed159e`
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
# Wed, 30 Nov 2022 21:24:32 GMT
ENV PG_MAJOR=15
# Wed, 30 Nov 2022 21:24:32 GMT
ENV PG_VERSION=15.1
# Wed, 30 Nov 2022 21:24:32 GMT
ENV PG_SHA256=64fdf23d734afad0dfe4077daca96ac51dcd697e68ae2d3d4ca6c45cb14e21ae
# Tue, 13 Dec 2022 23:01:58 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		nss_wrapper 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 13 Dec 2022 23:01:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 13 Dec 2022 23:01:59 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Dec 2022 23:02:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Dec 2022 23:02:00 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Dec 2022 23:02:00 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Dec 2022 23:02:00 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 13 Dec 2022 23:02:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Dec 2022 23:02:00 GMT
STOPSIGNAL SIGINT
# Tue, 13 Dec 2022 23:02:01 GMT
EXPOSE 5432
# Tue, 13 Dec 2022 23:02:01 GMT
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
	-	`sha256:a4e7269dfd19efad65705ac4d2ee51faeaac5bc65e6ad9f1fc2e1a8f9b94c101`  
		Last Modified: Tue, 13 Dec 2022 23:15:54 GMT  
		Size: 83.6 MB (83645744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4bbc7d23431a3f34c1d7fd8a9aff43da363c1bfa49689aee9de6753913a26be`  
		Last Modified: Tue, 13 Dec 2022 23:15:41 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1df89b0e2474aa93bb4780155a29e500a2343257eda163278f9d776483045a`  
		Last Modified: Tue, 13 Dec 2022 23:15:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d369d566a9c9475c9ac6c3818e05f2fa36931425d189208f0f73a5d2273232b7`  
		Last Modified: Tue, 13 Dec 2022 23:15:42 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89de6127c7bad84e9a5ba6d45b26c2b5d0d6730f650afb7426c7c00855c479dd`  
		Last Modified: Tue, 13 Dec 2022 23:15:42 GMT  
		Size: 4.7 KB (4699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:c42193d3d44c93d760a5a50d42508e0fd7ad726979f90120ef08a787f7b4b6d6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91809866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a624d89badde0f3c2940c259bd94d558c8490a6f8f7f685e8828d578a5ddc47`
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
# Wed, 30 Nov 2022 21:41:49 GMT
ENV PG_MAJOR=15
# Wed, 30 Nov 2022 21:41:49 GMT
ENV PG_VERSION=15.1
# Wed, 30 Nov 2022 21:41:49 GMT
ENV PG_SHA256=64fdf23d734afad0dfe4077daca96ac51dcd697e68ae2d3d4ca6c45cb14e21ae
# Tue, 13 Dec 2022 22:56:22 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		nss_wrapper 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 13 Dec 2022 22:56:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 13 Dec 2022 22:56:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Dec 2022 22:56:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Dec 2022 22:56:24 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Dec 2022 22:56:24 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Dec 2022 22:56:24 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 13 Dec 2022 22:56:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Dec 2022 22:56:24 GMT
STOPSIGNAL SIGINT
# Tue, 13 Dec 2022 22:56:24 GMT
EXPOSE 5432
# Tue, 13 Dec 2022 22:56:24 GMT
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
	-	`sha256:a98b0114406af5d3ebb211ea0a482258bfa307584fe51bc84e9c975feed3636f`  
		Last Modified: Tue, 13 Dec 2022 23:05:31 GMT  
		Size: 88.5 MB (88534735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db20b0395ad4cf97df41e409832952a0b508dbf67d9fd6de416b7435920abc1`  
		Last Modified: Tue, 13 Dec 2022 23:05:23 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c3f53a68890c98f1fa2726a370b553b49bc2f461e351263d71ae535f0c80037`  
		Last Modified: Tue, 13 Dec 2022 23:05:22 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3136ef726ed4a95fd800aecd43e0bf58590a6634c2ac5bfb671cce02a3e06e`  
		Last Modified: Tue, 13 Dec 2022 23:05:22 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663002c1aef941af29259c2e412c4095972273b394379d3e31a760307066eb74`  
		Last Modified: Tue, 13 Dec 2022 23:05:23 GMT  
		Size: 4.7 KB (4705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:alpine` - linux; 386

```console
$ docker pull postgres@sha256:d45f355602b4bf5a3121686b1e448f5c7f41003fecb47cecf471b8a98535d517
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98924729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b8bd10f847dc69500e66734140ac6129846a6f0cb03af39b86315241a1314f`
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
# Wed, 30 Nov 2022 20:46:35 GMT
ENV PG_MAJOR=15
# Wed, 30 Nov 2022 20:46:36 GMT
ENV PG_VERSION=15.1
# Wed, 30 Nov 2022 20:46:37 GMT
ENV PG_SHA256=64fdf23d734afad0dfe4077daca96ac51dcd697e68ae2d3d4ca6c45cb14e21ae
# Tue, 13 Dec 2022 23:06:26 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		nss_wrapper 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 13 Dec 2022 23:06:26 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 13 Dec 2022 23:06:27 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Dec 2022 23:06:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Dec 2022 23:06:29 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Dec 2022 23:06:30 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Dec 2022 23:06:32 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 13 Dec 2022 23:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Dec 2022 23:06:33 GMT
STOPSIGNAL SIGINT
# Tue, 13 Dec 2022 23:06:34 GMT
EXPOSE 5432
# Tue, 13 Dec 2022 23:06:35 GMT
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
	-	`sha256:969257085d29af7493525d7479e2a65fdd94e31ec8a9f514a2672779aa82191c`  
		Last Modified: Tue, 13 Dec 2022 23:20:52 GMT  
		Size: 95.5 MB (95500409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a95971f668ad589f35d3fe276953d0b93ccb277be5c1ef8b10b3d21bb5e2b1`  
		Last Modified: Tue, 13 Dec 2022 23:20:40 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d954092eae95bd961097cef964d6dbbaee05ea63e867a7b713d42673e6b3201c`  
		Last Modified: Tue, 13 Dec 2022 23:20:40 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4266555a0041b5e2d9096265c5bf598f0389572d9f2e4eee65c5a5e4017133b`  
		Last Modified: Tue, 13 Dec 2022 23:20:40 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e1a4f396f0646f1de1074a0da06a5fb8d6e3ac4e4e1e54ef0857b4849fb355`  
		Last Modified: Tue, 13 Dec 2022 23:20:40 GMT  
		Size: 4.7 KB (4702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:793a8b491cd31806b8f31b74edbc28d0c77cb37b35d1c902eca6fc5c5c96251a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99940917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac40d3d0b3095379c65e555435bd23cee454b2d6a582fae14e0b8d5a67775ab1`
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
# Wed, 30 Nov 2022 22:15:28 GMT
ENV PG_MAJOR=15
# Wed, 30 Nov 2022 22:15:28 GMT
ENV PG_VERSION=15.1
# Wed, 30 Nov 2022 22:15:28 GMT
ENV PG_SHA256=64fdf23d734afad0dfe4077daca96ac51dcd697e68ae2d3d4ca6c45cb14e21ae
# Wed, 30 Nov 2022 22:18:58 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 30 Nov 2022 22:19:02 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 30 Nov 2022 22:19:03 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 30 Nov 2022 22:19:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 30 Nov 2022 22:19:05 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 30 Nov 2022 22:19:06 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 30 Nov 2022 22:19:06 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Wed, 30 Nov 2022 22:19:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Nov 2022 22:19:07 GMT
STOPSIGNAL SIGINT
# Wed, 30 Nov 2022 22:19:07 GMT
EXPOSE 5432
# Wed, 30 Nov 2022 22:19:07 GMT
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
	-	`sha256:c1c9341c7eec5f0ef0f811f8bdc42ce2654bc398956c0a3e176627965223abde`  
		Last Modified: Wed, 30 Nov 2022 22:35:33 GMT  
		Size: 96.5 MB (96540462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d362fd98cdc94383ffafdee20f307bc9ff96c84629f8f23f5b6b771ad5b012c2`  
		Last Modified: Wed, 30 Nov 2022 22:35:11 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cd226e89e93d18de95995a527edec550a9f4bed6a4c8d58b89d0a5effda858`  
		Last Modified: Wed, 30 Nov 2022 22:35:11 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1ff3ca1bd9e41493be3687ed8316bbde9b7bb85497de31e6da31e274da55ca`  
		Last Modified: Wed, 30 Nov 2022 22:35:11 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29537a7e3fb0bc54570d42db8447d4e5c553a300600df14df2e58df0dd4a9ff`  
		Last Modified: Wed, 30 Nov 2022 22:35:11 GMT  
		Size: 4.7 KB (4707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:alpine` - linux; s390x

```console
$ docker pull postgres@sha256:135429e460a42899bd9be4ba2ce2a4be6b0e1dc4cbf73fc0296c2a75bc60c862
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94671979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ee4457ab7f0e077cd96ee00ae30680b1ecb57183c71a106ae2ec5454ac8b7e`
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
# Wed, 30 Nov 2022 21:25:41 GMT
ENV PG_MAJOR=15
# Wed, 30 Nov 2022 21:25:42 GMT
ENV PG_VERSION=15.1
# Wed, 30 Nov 2022 21:25:42 GMT
ENV PG_SHA256=64fdf23d734afad0dfe4077daca96ac51dcd697e68ae2d3d4ca6c45cb14e21ae
# Tue, 13 Dec 2022 23:08:07 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		nss_wrapper 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 13 Dec 2022 23:08:12 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 13 Dec 2022 23:08:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Dec 2022 23:08:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Dec 2022 23:08:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Dec 2022 23:08:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Dec 2022 23:08:13 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 13 Dec 2022 23:08:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Dec 2022 23:08:13 GMT
STOPSIGNAL SIGINT
# Tue, 13 Dec 2022 23:08:13 GMT
EXPOSE 5432
# Tue, 13 Dec 2022 23:08:14 GMT
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
	-	`sha256:a089de75d0b96134faf8266bdf2600f85268cb5b9e04e3ec3c1f91eaca4c585d`  
		Last Modified: Tue, 13 Dec 2022 23:35:02 GMT  
		Size: 91.5 MB (91485220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd58453c2f84bada8585f34f318f6ad6477b955a651c6f2a8d05b6eb6700f4f`  
		Last Modified: Tue, 13 Dec 2022 23:34:51 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1e0f6d5c78aa851c4ca8d1d64790939766a2518d2855373764d28b0ab100b0`  
		Last Modified: Tue, 13 Dec 2022 23:34:51 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538a546b50a8a347d05fbfcff57962fec4272c20dad2200a35c69d361e02d7af`  
		Last Modified: Tue, 13 Dec 2022 23:34:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863fe7403de9dd51b52f925da4e429e1f4c9bdbde752548f410bdb19c8eace71`  
		Last Modified: Tue, 13 Dec 2022 23:34:51 GMT  
		Size: 4.7 KB (4701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
