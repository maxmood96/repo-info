## `postgres:12-alpine`

```console
$ docker pull postgres@sha256:be5425972acbf7d04245d18bee00f88183e9af26538014618f432807fe5a9a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `postgres:12-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:35efa4561d8e40f10b87e3767f0cbf10d779ac6c14191e9d5c9c174b751e2df0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61990764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec50832fed06629e3f55275c3d9225a72eeb43339f4a18b028e8ae14ddc0e7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 15 Jan 2021 02:23:51 GMT
ADD file:edbe213ae0c825a5bfbe569928cf20f683f334f93a093ccd0a3a014b7428e760 in / 
# Fri, 15 Jan 2021 02:23:51 GMT
CMD ["/bin/sh"]
# Thu, 21 Jan 2021 19:35:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 21 Jan 2021 19:35:15 GMT
ENV LANG=en_US.utf8
# Thu, 21 Jan 2021 19:35:16 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 21 Jan 2021 19:42:42 GMT
ENV PG_MAJOR=12
# Thu, 21 Jan 2021 19:42:42 GMT
ENV PG_VERSION=12.5
# Thu, 21 Jan 2021 19:42:43 GMT
ENV PG_SHA256=bd0d25341d9578b5473c9506300022de26370879581f5fddd243a886ce79ff95
# Thu, 21 Jan 2021 19:49:45 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 21 Jan 2021 19:49:46 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 21 Jan 2021 19:49:47 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 21 Jan 2021 19:49:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Jan 2021 19:49:48 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 21 Jan 2021 19:49:49 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Jan 2021 19:49:49 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:49:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Jan 2021 19:49:49 GMT
STOPSIGNAL SIGINT
# Thu, 21 Jan 2021 19:49:49 GMT
EXPOSE 5432
# Thu, 21 Jan 2021 19:49:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:596ba82af5aaa3e2fd9d6f955b8b94f0744a2b60710e3c243ba3e4a467f051d1`  
		Last Modified: Fri, 15 Jan 2021 02:08:10 GMT  
		Size: 2.8 MB (2810825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8271b35503fb62bfa2f68a3a5f2f051276650964585403ee69453c552ecf5838`  
		Last Modified: Thu, 21 Jan 2021 20:13:16 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fde607c214b2eb1f39958d85758ee4a83c5caab88fd4deefb7e2e8d2985ce20`  
		Last Modified: Thu, 21 Jan 2021 20:13:16 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def7be17789e080fbf2ebb84947b21a22ad17aab9d4762c866fc808106178ce0`  
		Last Modified: Thu, 21 Jan 2021 20:14:01 GMT  
		Size: 59.2 MB (59165667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ea0883c333c1494e36710278da68e90bacbc6e4c9615bd702fd78be7e36186`  
		Last Modified: Thu, 21 Jan 2021 20:13:46 GMT  
		Size: 8.2 KB (8211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54629ca0949520f417f0c077101dd4c6d06588fcf05ec0bd09b4384db0850d82`  
		Last Modified: Thu, 21 Jan 2021 20:13:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b382cf34866ea8ad7aea100065abc2fd033ac8e30e0d561b209edd4ae305c4a2`  
		Last Modified: Thu, 21 Jan 2021 20:13:47 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9cb46d7648dea588a2cd498cc83f02577613c7000c3a2bd3dd61e94e45588a`  
		Last Modified: Thu, 21 Jan 2021 20:13:45 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:d4fd19bdb1c5913a64fc41b412f93b71211e6af88f21ac500610c420009aafb0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59978693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca43e0935a5680b1f78482998692fe7b48d9a8b30191fcec4d276d876ef5578e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 28 Jan 2021 23:49:59 GMT
ADD file:c197324e4979e2a7b257ad683d20dd9cbdae525a076bd68fe6aa0e0b126875df in / 
# Thu, 28 Jan 2021 23:49:59 GMT
CMD ["/bin/sh"]
# Fri, 29 Jan 2021 01:09:22 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 29 Jan 2021 01:09:23 GMT
ENV LANG=en_US.utf8
# Fri, 29 Jan 2021 01:09:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 29 Jan 2021 01:13:40 GMT
ENV PG_MAJOR=12
# Fri, 29 Jan 2021 01:13:41 GMT
ENV PG_VERSION=12.5
# Fri, 29 Jan 2021 01:13:42 GMT
ENV PG_SHA256=bd0d25341d9578b5473c9506300022de26370879581f5fddd243a886ce79ff95
# Fri, 29 Jan 2021 01:17:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 29 Jan 2021 01:17:28 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 29 Jan 2021 01:17:30 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 29 Jan 2021 01:17:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 29 Jan 2021 01:17:32 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 29 Jan 2021 01:17:33 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 29 Jan 2021 01:17:33 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Fri, 29 Jan 2021 01:17:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Jan 2021 01:17:35 GMT
STOPSIGNAL SIGINT
# Fri, 29 Jan 2021 01:17:35 GMT
EXPOSE 5432
# Fri, 29 Jan 2021 01:17:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a66f440da051140fefcb0a520bdeb69d763b1eb4fd1b2ed46b4c0a168e335108`  
		Last Modified: Thu, 28 Jan 2021 23:50:33 GMT  
		Size: 2.6 MB (2621759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47814bcbfb45802646b189af4a9bc3e4510a538b55fd2808df448ec5e6491cff`  
		Last Modified: Fri, 29 Jan 2021 01:32:14 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6e4686dd674a32664773b275c120c9879a27454fb70c89ea4663315c3b84c6`  
		Last Modified: Fri, 29 Jan 2021 01:32:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf27716a17c39edad69b8fe450ec5e57ad70e16768cb1f51348fec84580e1c9d`  
		Last Modified: Fri, 29 Jan 2021 01:33:02 GMT  
		Size: 57.3 MB (57342545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137e46bf975c09851067c7f4b7bc13b3f23199b29def606df4ddea28be65f03f`  
		Last Modified: Fri, 29 Jan 2021 01:32:43 GMT  
		Size: 8.2 KB (8207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de675533f76a4f92b35cc4558130e88dfa3e162cfc0059246e674d0f7d4b736`  
		Last Modified: Fri, 29 Jan 2021 01:32:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675a8e79b1a8ded333fc1cf4aed995f9f2b0333fbc03138c91939c2aabceda19`  
		Last Modified: Fri, 29 Jan 2021 01:32:43 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18314d6256ef4e3dc3551ab1d52e4956670b0cae65e4452d46870e95b84e068a`  
		Last Modified: Fri, 29 Jan 2021 01:32:43 GMT  
		Size: 4.4 KB (4405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:adea49d10edb4914b198062ad42818a289d33c7bfab1b30c95143180870830f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57035609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adf2427f115bea01ec549f140f72615f41c86684816a24129e7694a527c65fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 28 Jan 2021 23:58:03 GMT
ADD file:98a89b90a8b442eed5301790dd2bd3a27391c5e4426126eed9d1cf44e70f8857 in / 
# Thu, 28 Jan 2021 23:58:04 GMT
CMD ["/bin/sh"]
# Fri, 29 Jan 2021 01:46:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 29 Jan 2021 01:46:42 GMT
ENV LANG=en_US.utf8
# Fri, 29 Jan 2021 01:46:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 29 Jan 2021 01:51:08 GMT
ENV PG_MAJOR=12
# Fri, 29 Jan 2021 01:51:09 GMT
ENV PG_VERSION=12.5
# Fri, 29 Jan 2021 01:51:10 GMT
ENV PG_SHA256=bd0d25341d9578b5473c9506300022de26370879581f5fddd243a886ce79ff95
# Fri, 29 Jan 2021 01:54:31 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 29 Jan 2021 01:54:34 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 29 Jan 2021 01:54:37 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 29 Jan 2021 01:54:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 29 Jan 2021 01:54:43 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 29 Jan 2021 01:54:44 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 29 Jan 2021 01:54:45 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Fri, 29 Jan 2021 01:54:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Jan 2021 01:54:47 GMT
STOPSIGNAL SIGINT
# Fri, 29 Jan 2021 01:54:48 GMT
EXPOSE 5432
# Fri, 29 Jan 2021 01:54:49 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9b1db703a337d301b1d50292acfbabd5fb3796511b962410c554420b85cd78dc`  
		Last Modified: Thu, 28 Jan 2021 23:58:38 GMT  
		Size: 2.4 MB (2423559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7fa668b3d0ed9168e26ae186f3e531d3ae1e280d94f950446b3683eaaab37c8`  
		Last Modified: Fri, 29 Jan 2021 02:09:19 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f921cd3d5ba006be49bcfc3c119ff3d8f5d35fbc011e764afbbce4ee5b61b4`  
		Last Modified: Fri, 29 Jan 2021 02:09:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b70b8f2f9d3a2a2ed425f8bd8c83bc1f8569f6a9a6c236df35b48bb8f94c3ab`  
		Last Modified: Fri, 29 Jan 2021 02:09:56 GMT  
		Size: 54.6 MB (54597656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd8d2d64ae2749f83ff8e88a8ca6dae1b267c3c2a601e3edb89a9dfd040b1b1`  
		Last Modified: Fri, 29 Jan 2021 02:09:41 GMT  
		Size: 8.2 KB (8211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66b6fe2a0ebdbd8e2c9a36a8b7fea035e5c6f8b7988dc3b3b50ddc517f5e7af`  
		Last Modified: Fri, 29 Jan 2021 02:09:41 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d7f4d34ca5a3e71c53a1a9f3fee59a36216073a6eefbe9c52183ca833f9cc5`  
		Last Modified: Fri, 29 Jan 2021 02:09:41 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1db4aca4242f208741d54686dab07c6a63f0ced28533ba3d33411b96363491`  
		Last Modified: Fri, 29 Jan 2021 02:09:41 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:3c40caa88b13c03e66104ed608cd66f3840c9c02ac0302cf5d841235b3ba14df
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60905225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d9ecfdf840c4ab67c76e94b6c60d23ccf50aa67e08446bb4f560ce06de7b26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 28 Jan 2021 23:39:33 GMT
ADD file:fecabe41deaeb72acdd63023566d87ae48b013ef80c97fdd993b55d6c727da93 in / 
# Thu, 28 Jan 2021 23:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Jan 2021 00:52:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 29 Jan 2021 00:52:24 GMT
ENV LANG=en_US.utf8
# Fri, 29 Jan 2021 00:52:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 29 Jan 2021 00:56:34 GMT
ENV PG_MAJOR=12
# Fri, 29 Jan 2021 00:56:35 GMT
ENV PG_VERSION=12.5
# Fri, 29 Jan 2021 00:56:36 GMT
ENV PG_SHA256=bd0d25341d9578b5473c9506300022de26370879581f5fddd243a886ce79ff95
# Fri, 29 Jan 2021 01:00:06 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 29 Jan 2021 01:00:09 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 29 Jan 2021 01:00:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 29 Jan 2021 01:00:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 29 Jan 2021 01:00:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 29 Jan 2021 01:00:16 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 29 Jan 2021 01:00:17 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Fri, 29 Jan 2021 01:00:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Jan 2021 01:00:19 GMT
STOPSIGNAL SIGINT
# Fri, 29 Jan 2021 01:00:20 GMT
EXPOSE 5432
# Fri, 29 Jan 2021 01:00:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2914792bc417803b2106001990194cc00cdd4b6fd97cd21a368f26148bc8e722`  
		Last Modified: Thu, 28 Jan 2021 23:40:10 GMT  
		Size: 2.7 MB (2711261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84190c434223807f9b123dbab6b871f4d978fc7fcfb7bd372aae021a3f90b9cf`  
		Last Modified: Fri, 29 Jan 2021 01:16:24 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23887416d5dd038d93a43a59a6bc616f68e5f6805f3aadcedb9577d2274a5f0`  
		Last Modified: Fri, 29 Jan 2021 01:16:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63287ead0e86f564b727f983763711773cf62527791c57a738c5d6f0e6ed5419`  
		Last Modified: Fri, 29 Jan 2021 01:17:05 GMT  
		Size: 58.2 MB (58179570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5460735eddbd6b6b248a4801de1fdbbe333f24e2b0e1c5df429a0f3599bbbc`  
		Last Modified: Fri, 29 Jan 2021 01:16:51 GMT  
		Size: 8.2 KB (8207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cf2ca5467bcab74fe0b446d5590bf7948634605350fed86b2fb3f8d7133380`  
		Last Modified: Fri, 29 Jan 2021 01:16:51 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822bef33597d2a055d86165830cdc710130a7ae4cb9dfe7440b776f41adaeaaa`  
		Last Modified: Fri, 29 Jan 2021 01:16:51 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390dd6fbf81e8ceefb931171c5764ee468f5f8e32acb10eb3328b7d66a79e396`  
		Last Modified: Fri, 29 Jan 2021 01:16:51 GMT  
		Size: 4.4 KB (4405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine` - linux; 386

```console
$ docker pull postgres@sha256:b58b4fee9f9fb5beeb7875e7ac4b5b281151cae01cacefbbd8a7a5a9431cd008
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65518922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d0f50affa436f6b0c69670a322fb8ebda948b0a21c128ff8e6735bbb0450ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 15 Jan 2021 01:38:28 GMT
ADD file:d8723c02f1eb0efa4dadc6480a753d18d7e28d9815bff96a92ff09ff55a92b11 in / 
# Fri, 15 Jan 2021 01:38:29 GMT
CMD ["/bin/sh"]
# Thu, 21 Jan 2021 20:03:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 21 Jan 2021 20:03:48 GMT
ENV LANG=en_US.utf8
# Thu, 21 Jan 2021 20:03:48 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 21 Jan 2021 20:15:03 GMT
ENV PG_MAJOR=12
# Thu, 21 Jan 2021 20:15:03 GMT
ENV PG_VERSION=12.5
# Thu, 21 Jan 2021 20:15:03 GMT
ENV PG_SHA256=bd0d25341d9578b5473c9506300022de26370879581f5fddd243a886ce79ff95
# Thu, 21 Jan 2021 20:23:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 21 Jan 2021 20:23:16 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 21 Jan 2021 20:23:17 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 21 Jan 2021 20:23:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Jan 2021 20:23:18 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 21 Jan 2021 20:23:18 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Jan 2021 20:23:18 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 21 Jan 2021 20:23:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Jan 2021 20:23:19 GMT
STOPSIGNAL SIGINT
# Thu, 21 Jan 2021 20:23:19 GMT
EXPOSE 5432
# Thu, 21 Jan 2021 20:23:19 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9e6a151110e36daa7a487250f98425289313f856e3a586d89d82bafc1bf322c3`  
		Last Modified: Fri, 15 Jan 2021 01:39:01 GMT  
		Size: 2.8 MB (2817152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c3db689820658689c81b40f398df66e73386faab62653de4807455bee50ea0`  
		Last Modified: Thu, 21 Jan 2021 20:46:44 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:badbf29d5646cafbfaa74149552c9058f0de90cb02ab656f20d8b3ca83193755`  
		Last Modified: Thu, 21 Jan 2021 20:46:44 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa3195c6141e0692908df603a6feb5f1a24e76cc5012ec56873ce6e3d8beff6`  
		Last Modified: Thu, 21 Jan 2021 20:47:31 GMT  
		Size: 62.7 MB (62687501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad2d907fef0bd0bdd5f678e22da90fab3146893c430e0ff5cc14fd7d0436cbc`  
		Last Modified: Thu, 21 Jan 2021 20:47:14 GMT  
		Size: 8.2 KB (8208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204a044fe9e379b35380ecbb7197037322d9efe7fe157faad6a3012b6db2f2f7`  
		Last Modified: Thu, 21 Jan 2021 20:47:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf92bcc3fd279df8ddf50852aeee63d48d7ccaf1dda6c695f8d49024c3e8bfbb`  
		Last Modified: Thu, 21 Jan 2021 20:47:14 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7c36871750838aaab6b96bcb7e6072b1592b1a01b18ce8ae048a16a7e34418`  
		Last Modified: Thu, 21 Jan 2021 20:47:14 GMT  
		Size: 4.4 KB (4404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:695894d0ed8e53ab19c838ac6da057852c201f149f841ed710bdf8ac52a7c7ae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63991726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d34f7437edd2af1bd29801a5a820e37de2ebc3d09733c10918066a9db1b54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 28 Jan 2021 23:55:50 GMT
ADD file:b14fd5f3f7fcd16e2b4ec6932d3e9c07c7400c577cee5fdcb88b0795a70a7bfb in / 
# Thu, 28 Jan 2021 23:55:52 GMT
CMD ["/bin/sh"]
# Fri, 29 Jan 2021 01:48:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 29 Jan 2021 01:48:55 GMT
ENV LANG=en_US.utf8
# Fri, 29 Jan 2021 01:49:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 29 Jan 2021 01:55:55 GMT
ENV PG_MAJOR=12
# Fri, 29 Jan 2021 01:56:05 GMT
ENV PG_VERSION=12.5
# Fri, 29 Jan 2021 01:56:12 GMT
ENV PG_SHA256=bd0d25341d9578b5473c9506300022de26370879581f5fddd243a886ce79ff95
# Fri, 29 Jan 2021 02:00:34 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 29 Jan 2021 02:01:06 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 29 Jan 2021 02:01:30 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 29 Jan 2021 02:01:34 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 29 Jan 2021 02:01:43 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 29 Jan 2021 02:01:57 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 29 Jan 2021 02:02:01 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Fri, 29 Jan 2021 02:02:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Jan 2021 02:02:15 GMT
STOPSIGNAL SIGINT
# Fri, 29 Jan 2021 02:02:30 GMT
EXPOSE 5432
# Fri, 29 Jan 2021 02:02:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f3b94a1d8d591af02f1b419642bee91066ecbb9c65099d6903deed310fd1c2ff`  
		Last Modified: Thu, 28 Jan 2021 23:56:32 GMT  
		Size: 2.8 MB (2812517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff06bd42b80b365bb0c19fbbbe316a95812c98b5963e0930ea89cc0c684a2833`  
		Last Modified: Fri, 29 Jan 2021 02:26:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf320aafe224f5aad678f29f514b47d6d4aefcd42e80b7041098c1da820f8c23`  
		Last Modified: Fri, 29 Jan 2021 02:26:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09d293792d50434549d0bb17dc9d332bac5863499e997793d8a56db7c3eda8a`  
		Last Modified: Fri, 29 Jan 2021 02:26:54 GMT  
		Size: 61.2 MB (61164807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f913bec7ebe2f1d924c7c574d707bb5ecf74f122fa009d3d4a3b28bcae74f0c0`  
		Last Modified: Fri, 29 Jan 2021 02:26:41 GMT  
		Size: 8.2 KB (8208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd46b36ad4546205c83a02a54af14f44eae8edda404bc8058b3ed5c92d8939c`  
		Last Modified: Fri, 29 Jan 2021 02:26:42 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1850996c2a7a91339a193e51470b0f90ff0cf57ae6b3f629dbecc9df410ea1d3`  
		Last Modified: Fri, 29 Jan 2021 02:26:41 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac15dae23d61c0eb456f0bcd548f3a1d09ee496d384a3e2e958297c32b7de30`  
		Last Modified: Fri, 29 Jan 2021 02:26:41 GMT  
		Size: 4.4 KB (4408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:a1485a4c00fec7badd741abee2a5ea1393aa707c8e708be6bde96d8917cc3eb5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64221667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1d81c09a5c64eb6d182ab7db260d7c1e417c4635e551adcaf3b00d1b9e66b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 28 Jan 2021 23:41:35 GMT
ADD file:d97e6c37df0fb8306b072d9c0a32f68f5aff583ba849303926644deacfa25eb9 in / 
# Thu, 28 Jan 2021 23:41:36 GMT
CMD ["/bin/sh"]
# Fri, 29 Jan 2021 01:28:50 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 29 Jan 2021 01:28:50 GMT
ENV LANG=en_US.utf8
# Fri, 29 Jan 2021 01:28:52 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 29 Jan 2021 01:33:30 GMT
ENV PG_MAJOR=12
# Fri, 29 Jan 2021 01:33:30 GMT
ENV PG_VERSION=12.5
# Fri, 29 Jan 2021 01:33:31 GMT
ENV PG_SHA256=bd0d25341d9578b5473c9506300022de26370879581f5fddd243a886ce79ff95
# Fri, 29 Jan 2021 01:37:27 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 29 Jan 2021 01:37:34 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 29 Jan 2021 01:37:36 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 29 Jan 2021 01:37:36 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 29 Jan 2021 01:37:37 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 29 Jan 2021 01:37:38 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 29 Jan 2021 01:37:38 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Fri, 29 Jan 2021 01:37:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Jan 2021 01:37:39 GMT
STOPSIGNAL SIGINT
# Fri, 29 Jan 2021 01:37:40 GMT
EXPOSE 5432
# Fri, 29 Jan 2021 01:37:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:43901f1af0ef9db6b0bf30ac6f6dacd78bf1ecfeb47ad0a93aa2370fa8e62407`  
		Last Modified: Thu, 28 Jan 2021 23:42:09 GMT  
		Size: 2.6 MB (2602059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb7987d6a49388c77e555f2547e538d557a90c40b705e0fe10a7ef952d82326`  
		Last Modified: Fri, 29 Jan 2021 01:50:33 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d07431bbbdfa6c1540603fded3d65695c350f29a3aa77a1e475296db695a5a`  
		Last Modified: Fri, 29 Jan 2021 01:50:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6b120532517fed3878855c0efab7d2f097d194b9ac69dc171cf94bbde299a3`  
		Last Modified: Fri, 29 Jan 2021 01:50:57 GMT  
		Size: 61.6 MB (61605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c1192f686294768a89edaf62a3179a0bf3dc1fa5c9d1e8abad825bdf1c62e9`  
		Last Modified: Fri, 29 Jan 2021 01:50:49 GMT  
		Size: 8.2 KB (8214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d919c36f862b0b8b073fef96d501c49a0209c701ebf51d70046b094c3db69b6`  
		Last Modified: Fri, 29 Jan 2021 01:50:49 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fed4d8709fdaf430849995591dd3264929602a03ef7d7aa3b701cc6fc84813a`  
		Last Modified: Fri, 29 Jan 2021 01:50:49 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb6da8610c12814a6374b15757c6cabb0e5e39c720d57d68b1bfd0e986481e2`  
		Last Modified: Fri, 29 Jan 2021 01:50:49 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
