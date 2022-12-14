## `postgres:13-alpine3.17`

```console
$ docker pull postgres@sha256:3babf16bde1c667205c8b6a7fa5550d78474a03d19fddeb3131f2f87b61dd6df
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

### `postgres:13-alpine3.17` - linux; amd64

```console
$ docker pull postgres@sha256:f98187f7db9420506702ff3be2738f74b7988e5d3f81a7a3f67d4ebec4ef31e3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (91974081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5d7ce47523e121c49952b3f557419605435f47dac2fa2071ad142938eebb35`
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
# Wed, 30 Nov 2022 22:15:31 GMT
ENV PG_MAJOR=13
# Wed, 30 Nov 2022 22:15:31 GMT
ENV PG_VERSION=13.9
# Wed, 30 Nov 2022 22:15:32 GMT
ENV PG_SHA256=ef1966c0a5e49fbed3370ad2824928cb6b1164617aeeae1606da283f7f33a415
# Tue, 13 Dec 2022 23:34:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		nss_wrapper 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 13 Dec 2022 23:34:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 13 Dec 2022 23:34:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Dec 2022 23:34:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Dec 2022 23:34:16 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Dec 2022 23:34:16 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Dec 2022 23:34:16 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 13 Dec 2022 23:34:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Dec 2022 23:34:16 GMT
STOPSIGNAL SIGINT
# Tue, 13 Dec 2022 23:34:16 GMT
EXPOSE 5432
# Tue, 13 Dec 2022 23:34:16 GMT
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
	-	`sha256:5210e1954950fbe9518573d9c750177922955943f308021b083e10ae3fe7aedc`  
		Last Modified: Tue, 13 Dec 2022 23:41:30 GMT  
		Size: 88.6 MB (88587852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841a11218bfcad89bd378a468c15f24def7915773c557382905318984d5ca055`  
		Last Modified: Tue, 13 Dec 2022 23:41:18 GMT  
		Size: 9.0 KB (9026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a4710be0f0a0499c8654cbf6eeb3be137a600a4686d85eebad037768017c6e`  
		Last Modified: Tue, 13 Dec 2022 23:41:18 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d265f5cca74f9fc81e84cf4ba6e5385d9981618ab8635c61af95c5f5c30e08`  
		Last Modified: Tue, 13 Dec 2022 23:41:18 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5697865d7a5b5d99d5fb1ee8babb22f56bdfce0316774e48122a4bb19d810da3`  
		Last Modified: Tue, 13 Dec 2022 23:41:18 GMT  
		Size: 4.7 KB (4702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine3.17` - linux; arm variant v6

```console
$ docker pull postgres@sha256:b864a154c1144c78d96bb3a5f86fa40455a98e450996efb3da6f12b1b55e05c9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89791205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21017cd36f6fff03c7cc34f9fbedf7b8eb57979bd5e17834ddc3bf0004eb63b`
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
# Wed, 30 Nov 2022 21:17:28 GMT
ENV PG_MAJOR=13
# Wed, 30 Nov 2022 21:17:29 GMT
ENV PG_VERSION=13.9
# Wed, 30 Nov 2022 21:17:29 GMT
ENV PG_SHA256=ef1966c0a5e49fbed3370ad2824928cb6b1164617aeeae1606da283f7f33a415
# Tue, 13 Dec 2022 23:21:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		nss_wrapper 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 13 Dec 2022 23:21:45 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 13 Dec 2022 23:21:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Dec 2022 23:21:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Dec 2022 23:21:47 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Dec 2022 23:21:47 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Dec 2022 23:21:47 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 13 Dec 2022 23:21:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Dec 2022 23:21:47 GMT
STOPSIGNAL SIGINT
# Tue, 13 Dec 2022 23:21:47 GMT
EXPOSE 5432
# Tue, 13 Dec 2022 23:21:48 GMT
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
	-	`sha256:0c66b48e4ec12fe7153195f5c0aff80f7b70023153af0c404aa0caae3b22284b`  
		Last Modified: Tue, 13 Dec 2022 23:31:12 GMT  
		Size: 86.7 MB (86668684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7101ef4d8b7f24fc10b14f7806b0db91facb2bec34d9c837bb2ab268b023c4af`  
		Last Modified: Tue, 13 Dec 2022 23:30:57 GMT  
		Size: 9.0 KB (9021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb05f0843e22bcbb0a555d1260f387f1c46bcc892e69d602a81763442105175c`  
		Last Modified: Tue, 13 Dec 2022 23:30:56 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5afec88a960da9de309099d2299255f47d0544f17d44fbd6e90736a04248e6fe`  
		Last Modified: Tue, 13 Dec 2022 23:30:56 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556813aa5cc44cb8ca4c2398fc6dc115c0d6cb0e863e7ca72375fe42268fa986`  
		Last Modified: Tue, 13 Dec 2022 23:30:56 GMT  
		Size: 4.7 KB (4699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine3.17` - linux; arm variant v7

```console
$ docker pull postgres@sha256:f27ba4a0dfdb131279d95c6e5c7dda4c0598bd8e840f876ee8f4b38935b909bd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84484991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a56abc8e5967de1ff958e204a9d67e6e697c3ec29100d1af33c7fb0fb651ee2f`
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
# Wed, 30 Nov 2022 21:31:11 GMT
ENV PG_MAJOR=13
# Wed, 30 Nov 2022 21:31:11 GMT
ENV PG_VERSION=13.9
# Wed, 30 Nov 2022 21:31:11 GMT
ENV PG_SHA256=ef1966c0a5e49fbed3370ad2824928cb6b1164617aeeae1606da283f7f33a415
# Tue, 13 Dec 2022 23:07:42 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		nss_wrapper 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 13 Dec 2022 23:07:43 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 13 Dec 2022 23:07:44 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Dec 2022 23:07:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Dec 2022 23:07:44 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Dec 2022 23:07:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Dec 2022 23:07:44 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 13 Dec 2022 23:07:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Dec 2022 23:07:45 GMT
STOPSIGNAL SIGINT
# Tue, 13 Dec 2022 23:07:45 GMT
EXPOSE 5432
# Tue, 13 Dec 2022 23:07:45 GMT
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
	-	`sha256:4aa6db8aee27799ea872592728889a1088d5be465b81c912317a1972efeb0168`  
		Last Modified: Tue, 13 Dec 2022 23:17:15 GMT  
		Size: 81.6 MB (81604254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541a76531c893f685180c21594355398949bebdac11c36d44254417e74e0a8d7`  
		Last Modified: Tue, 13 Dec 2022 23:17:01 GMT  
		Size: 9.0 KB (9020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f773802729f06928ec50c4ba4459ef9f10a89d20590920cb6573db2d0a43a5`  
		Last Modified: Tue, 13 Dec 2022 23:17:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd33c764ef90ddac000ffcaaab3525fbdb62000cd56635463c351b372a5561a`  
		Last Modified: Tue, 13 Dec 2022 23:17:05 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8370bf28903f5be51a69c66db45c5f17450108981265a14b6fdf62ce58c45337`  
		Last Modified: Tue, 13 Dec 2022 23:17:01 GMT  
		Size: 4.7 KB (4704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:9f5928e6714bdbd69d0b910900a5f6c6f3ff70e2b6b5aaf5b2c1a69e60805160
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89744757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a27ab764cf1db6bd8f65beefc1881d0b8163389ce829ae0e146b2b7945dc97`
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
# Wed, 30 Nov 2022 21:46:08 GMT
ENV PG_MAJOR=13
# Wed, 30 Nov 2022 21:46:08 GMT
ENV PG_VERSION=13.9
# Wed, 30 Nov 2022 21:46:08 GMT
ENV PG_SHA256=ef1966c0a5e49fbed3370ad2824928cb6b1164617aeeae1606da283f7f33a415
# Tue, 13 Dec 2022 23:00:32 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		nss_wrapper 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 13 Dec 2022 23:00:33 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 13 Dec 2022 23:00:34 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Dec 2022 23:00:34 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Dec 2022 23:00:34 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Dec 2022 23:00:34 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Dec 2022 23:00:34 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 13 Dec 2022 23:00:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Dec 2022 23:00:34 GMT
STOPSIGNAL SIGINT
# Tue, 13 Dec 2022 23:00:35 GMT
EXPOSE 5432
# Tue, 13 Dec 2022 23:00:35 GMT
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
	-	`sha256:7a08fb1616b9e3eed3a4058daac4aae5483658ac384ede88a9b6264cfe9caa85`  
		Last Modified: Tue, 13 Dec 2022 23:06:25 GMT  
		Size: 86.5 MB (86470059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cd299d0fe55c8d6a6216426cf6ed00f03038df62e9ff157758edb2df48fe98`  
		Last Modified: Tue, 13 Dec 2022 23:06:17 GMT  
		Size: 9.0 KB (9019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b199bb8e3f9fda0479bf00c5424cd7a0beeb01af8be6c9657209e35af4a2db`  
		Last Modified: Tue, 13 Dec 2022 23:06:17 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc91b25922fd2ccba1cc09e402330d289e40bdadbb7001daf04ced90c860dccf`  
		Last Modified: Tue, 13 Dec 2022 23:06:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f28f33aa901c2eace0f10d17d902a58a8cbac86cdab94dfb1aa2639d08e058`  
		Last Modified: Tue, 13 Dec 2022 23:06:17 GMT  
		Size: 4.7 KB (4701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine3.17` - linux; 386

```console
$ docker pull postgres@sha256:6909145227806892767e01d94888faf33ac1b8f57b9bfaefb38425479bc655c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96731237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bde44c1cf6a9c897136944f6e288de79e33f7ba53bb99f44e7b6be81bff5c6`
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
# Wed, 30 Nov 2022 20:53:22 GMT
ENV PG_MAJOR=13
# Wed, 30 Nov 2022 20:53:23 GMT
ENV PG_VERSION=13.9
# Wed, 30 Nov 2022 20:53:24 GMT
ENV PG_SHA256=ef1966c0a5e49fbed3370ad2824928cb6b1164617aeeae1606da283f7f33a415
# Tue, 13 Dec 2022 23:12:49 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		nss_wrapper 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 13 Dec 2022 23:12:50 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 13 Dec 2022 23:12:51 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Dec 2022 23:12:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Dec 2022 23:12:53 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Dec 2022 23:12:54 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Dec 2022 23:12:56 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 13 Dec 2022 23:12:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Dec 2022 23:12:57 GMT
STOPSIGNAL SIGINT
# Tue, 13 Dec 2022 23:12:58 GMT
EXPOSE 5432
# Tue, 13 Dec 2022 23:12:59 GMT
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
	-	`sha256:080e461dbaaab227fb5394dba2425ca2c84ecbe14508d05a77f4408e0e7462eb`  
		Last Modified: Tue, 13 Dec 2022 23:21:58 GMT  
		Size: 93.3 MB (93307344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26297335d0d9d86aa447264e33c308bf95a59c5497b7ae2d82b44487a2a07ed`  
		Last Modified: Tue, 13 Dec 2022 23:21:47 GMT  
		Size: 9.0 KB (9022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b0ff4efe51f3a5b5ad22e357bb4e299baa4cc9bbaaedf89ba8da4fa6340790`  
		Last Modified: Tue, 13 Dec 2022 23:21:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4372b2e4e47477fdec5a98465757539003862b6a8e1a2550adf8f60f40a30c`  
		Last Modified: Tue, 13 Dec 2022 23:21:47 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8950cdd60a8c951bdbd4a588268ec7d2d6ff33fcf33799eda967cffa86b75a`  
		Last Modified: Tue, 13 Dec 2022 23:21:47 GMT  
		Size: 4.7 KB (4701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine3.17` - linux; ppc64le

```console
$ docker pull postgres@sha256:3211e1898d90ee982e01771612bae3a1e3893b282c9e60fe22625dcc92156f5d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97673284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7319f19856180a772e90833d3c1709f9c748f4403337a164b888ae7293074d`
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
# Wed, 30 Nov 2022 22:23:12 GMT
ENV PG_MAJOR=13
# Wed, 30 Nov 2022 22:23:12 GMT
ENV PG_VERSION=13.9
# Wed, 30 Nov 2022 22:23:13 GMT
ENV PG_SHA256=ef1966c0a5e49fbed3370ad2824928cb6b1164617aeeae1606da283f7f33a415
# Wed, 30 Nov 2022 22:26:21 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 30 Nov 2022 22:26:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 30 Nov 2022 22:26:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 30 Nov 2022 22:26:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 30 Nov 2022 22:26:28 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 30 Nov 2022 22:26:28 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 30 Nov 2022 22:26:28 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Wed, 30 Nov 2022 22:26:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Nov 2022 22:26:29 GMT
STOPSIGNAL SIGINT
# Wed, 30 Nov 2022 22:26:29 GMT
EXPOSE 5432
# Wed, 30 Nov 2022 22:26:30 GMT
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
	-	`sha256:3a0d7a03c76077d3946568592288a77a6394ba9c013e60ee9978645288505dfd`  
		Last Modified: Wed, 30 Nov 2022 22:37:04 GMT  
		Size: 94.3 MB (94273260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac08319ae78f9c4f6d2c41d3650b17562e08eaabc8bc281e6dafa58467b27c50`  
		Last Modified: Wed, 30 Nov 2022 22:36:42 GMT  
		Size: 9.0 KB (9031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3049f17451d8963776be8018a64b912f6f2d2dd06058fc068d1d5f0ff4f1f3bc`  
		Last Modified: Wed, 30 Nov 2022 22:36:43 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb4ca352f850ffc75e27d5b0ef2bb14d5e4c9d9dc34bb6fccfcc7fe9c6abcf`  
		Last Modified: Wed, 30 Nov 2022 22:36:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0f2f8758158fcb60b12e9521e124c83b2a14ad4bdb1f9ad99f74c7bab0fab4`  
		Last Modified: Wed, 30 Nov 2022 22:36:42 GMT  
		Size: 4.7 KB (4701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine3.17` - linux; s390x

```console
$ docker pull postgres@sha256:e2314716819ec657dc563406b62c287044838ed788945a8dc52ebc416318c970
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92520726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e63a813fb750e3b7554b790b91e33c05c983d6d8a02386311fba50b6cd4bee`
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
# Wed, 30 Nov 2022 21:31:37 GMT
ENV PG_MAJOR=13
# Wed, 30 Nov 2022 21:31:37 GMT
ENV PG_VERSION=13.9
# Wed, 30 Nov 2022 21:31:37 GMT
ENV PG_SHA256=ef1966c0a5e49fbed3370ad2824928cb6b1164617aeeae1606da283f7f33a415
# Tue, 13 Dec 2022 23:15:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		nss_wrapper 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 13 Dec 2022 23:15:19 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 13 Dec 2022 23:15:20 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Dec 2022 23:15:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Dec 2022 23:15:21 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Dec 2022 23:15:22 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Dec 2022 23:15:22 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 13 Dec 2022 23:15:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Dec 2022 23:15:23 GMT
STOPSIGNAL SIGINT
# Tue, 13 Dec 2022 23:15:24 GMT
EXPOSE 5432
# Tue, 13 Dec 2022 23:15:24 GMT
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
	-	`sha256:eda5031352c71a2dbbac5143ffdf42436c69821834bc9cb9e466c5f99f1a7ba0`  
		Last Modified: Tue, 13 Dec 2022 23:36:01 GMT  
		Size: 89.3 MB (89334396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98206c292adf87d9bd59387a5a4586c18f3cb7000df5d2380990f4aa06ed8854`  
		Last Modified: Tue, 13 Dec 2022 23:35:50 GMT  
		Size: 9.0 KB (9024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af673e635dbe3db4e7ead35babb1a593e55aee5e67f20b7161eeae59d23e8912`  
		Last Modified: Tue, 13 Dec 2022 23:35:50 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5429c4603469607cdba9cc333d0d4eb91b5eeec29f0bf186b26e8595eed7cd`  
		Last Modified: Tue, 13 Dec 2022 23:35:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76d2dfe0dc394fe65ae0d35837bd84befcf2be9056c87e4a3fbd3a5122f1852`  
		Last Modified: Tue, 13 Dec 2022 23:35:50 GMT  
		Size: 4.7 KB (4703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
