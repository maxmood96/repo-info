## `postgres:9-alpine`

```console
$ docker pull postgres@sha256:340e61a5d4bef6357d3aac153708eb3839e023b12ca8e9a2986f8b94e5d91bbf
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

### `postgres:9-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:c2b558c811efb0c3d917c0915536b8970ad0c56c2af0dde5620f1bd8187c3e87
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14359262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5116b8393895a0512c1cf24cdccdb4aa46c774ab0bf52866f3c0895e479b4aa8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 07:55:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 22 Oct 2020 07:55:14 GMT
ENV LANG=en_US.utf8
# Thu, 22 Oct 2020 07:55:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Oct 2020 08:15:43 GMT
ENV PG_MAJOR=9.6
# Fri, 13 Nov 2020 02:49:29 GMT
ENV PG_VERSION=9.6.20
# Fri, 13 Nov 2020 02:49:30 GMT
ENV PG_SHA256=3d08cba409d45ab62d42b24431a0d55e7537bcd1db2d979f5f2eefe34d487bb6
# Fri, 13 Nov 2020 02:53:22 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 13 Nov 2020 02:53:24 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 13 Nov 2020 02:53:25 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 13 Nov 2020 02:53:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 13 Nov 2020 02:53:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 13 Nov 2020 02:53:26 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 13 Nov 2020 02:53:26 GMT
COPY file:be0996fe6c3fcec9976408f3f94ed203fdcb751cfa2cd940a2bfcbbbda925e9c in /usr/local/bin/ 
# Fri, 13 Nov 2020 02:53:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 13 Nov 2020 02:53:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Nov 2020 02:53:28 GMT
STOPSIGNAL SIGINT
# Fri, 13 Nov 2020 02:53:28 GMT
EXPOSE 5432
# Fri, 13 Nov 2020 02:53:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f1d1b70e7fa650fd6229086120f763219adce9e33e8b20bdfbf8452ab69847`  
		Last Modified: Thu, 22 Oct 2020 08:21:53 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4f01476d2b86761cdb0414c4a583b89af3b5d0b67022cfc0d378743307f7e3`  
		Last Modified: Thu, 22 Oct 2020 08:21:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db9cf10d1b35705117c15ea9b43d1b0bf12ae3bc5744ebe44a44448c843d170b`  
		Last Modified: Fri, 13 Nov 2020 03:03:31 GMT  
		Size: 11.5 MB (11549205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9e498a3afe58efc477f75763e814c4bd828170281c0c3e2399e79e6fb2fdae`  
		Last Modified: Fri, 13 Nov 2020 03:03:26 GMT  
		Size: 7.2 KB (7159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c95856cb079ca9925b7291c2615a229ae3099725d558d98ee431d072701207`  
		Last Modified: Fri, 13 Nov 2020 03:03:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6331d57c1af947cb3570d12ba0e7e750f65a4ceb89a2f529b11eb95903820f`  
		Last Modified: Fri, 13 Nov 2020 03:03:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3623f4ffd59741394a58e4ce1a4c30b8bd9616af314bc66fe734fa30374bb9`  
		Last Modified: Fri, 13 Nov 2020 03:03:27 GMT  
		Size: 4.3 KB (4259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f99cd0e31168884b7ee2bc7afd9b17ad6c8e8738c7994b225278b2100479f84`  
		Last Modified: Fri, 13 Nov 2020 03:03:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:67d073a22cc1ecf823342968c0d242d0f4a8e7ac9290189dcad431a3a705696f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13718476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8b35083692d61e66c3157a2a960622765bb87839169319b5b053e98be97551`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 08:55:00 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 22 Oct 2020 08:55:00 GMT
ENV LANG=en_US.utf8
# Thu, 22 Oct 2020 08:55:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Oct 2020 09:12:58 GMT
ENV PG_MAJOR=9.6
# Thu, 22 Oct 2020 09:12:59 GMT
ENV PG_VERSION=9.6.19
# Thu, 22 Oct 2020 09:13:01 GMT
ENV PG_SHA256=61f93a94ccddbe0b2d1afaf03f04ba605d8af5b774ff9b830e5adeb50ab55cb0
# Thu, 22 Oct 2020 09:15:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 22 Oct 2020 09:15:42 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 22 Oct 2020 09:15:44 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 22 Oct 2020 09:15:45 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 Oct 2020 09:15:47 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 22 Oct 2020 09:15:47 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Oct 2020 09:15:48 GMT
COPY file:be0996fe6c3fcec9976408f3f94ed203fdcb751cfa2cd940a2bfcbbbda925e9c in /usr/local/bin/ 
# Thu, 22 Oct 2020 09:15:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 22 Oct 2020 09:15:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 09:15:51 GMT
STOPSIGNAL SIGINT
# Thu, 22 Oct 2020 09:15:52 GMT
EXPOSE 5432
# Thu, 22 Oct 2020 09:15:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54bc8a79538fa79db3e734327f2a73654bc80285dc55b7e4d8d206161ec79a9`  
		Last Modified: Thu, 22 Oct 2020 09:19:19 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30574d1822b9e42c2a6da5e4a8f52ab65d88be941e497b4565382967ebd326f8`  
		Last Modified: Thu, 22 Oct 2020 09:19:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0353861e0ba1303d75caddfcb98a9514a897fe1ad27e9987c30a038cafbd1f84`  
		Last Modified: Thu, 22 Oct 2020 09:21:05 GMT  
		Size: 11.1 MB (11103240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce900d8cdd76c363e93b952488d855f4db7edb56bf18586738c5155f8910ace6`  
		Last Modified: Thu, 22 Oct 2020 09:21:00 GMT  
		Size: 7.2 KB (7161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dd112bb8267e5d8120d52615ddb45fd149620202073d31cfd1c36d0a86d228`  
		Last Modified: Thu, 22 Oct 2020 09:20:59 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3a661aa047f8b6ad5f4e69ebc039a6b94736286292ec99afefc4944e9af6ca`  
		Last Modified: Thu, 22 Oct 2020 09:20:59 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a5519058f3c71aef9b7348fa7b0d319bb82301bc374264b0dcb8ee465ac34e`  
		Last Modified: Thu, 22 Oct 2020 09:20:59 GMT  
		Size: 4.3 KB (4262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abfb45db984f06c99a205023cb282cf565f493ad241b33c248bc9547ffa3bd8`  
		Last Modified: Thu, 22 Oct 2020 09:20:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:5369e2dde1cc60cd45d12d0028a321560d01b1bd24d1b90262724220fc95afee
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12860723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64969ad89255630ecd8302a86d3682899e4a62a17af13c7458cb08a946391ebc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 08:56:01 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 22 Oct 2020 08:56:03 GMT
ENV LANG=en_US.utf8
# Thu, 22 Oct 2020 08:56:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Oct 2020 09:10:47 GMT
ENV PG_MAJOR=9.6
# Thu, 22 Oct 2020 09:10:48 GMT
ENV PG_VERSION=9.6.19
# Thu, 22 Oct 2020 09:10:49 GMT
ENV PG_SHA256=61f93a94ccddbe0b2d1afaf03f04ba605d8af5b774ff9b830e5adeb50ab55cb0
# Thu, 22 Oct 2020 09:12:57 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 22 Oct 2020 09:13:01 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 22 Oct 2020 09:13:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 22 Oct 2020 09:13:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 Oct 2020 09:13:09 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 22 Oct 2020 09:13:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Oct 2020 09:13:12 GMT
COPY file:be0996fe6c3fcec9976408f3f94ed203fdcb751cfa2cd940a2bfcbbbda925e9c in /usr/local/bin/ 
# Thu, 22 Oct 2020 09:13:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 22 Oct 2020 09:13:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 09:13:17 GMT
STOPSIGNAL SIGINT
# Thu, 22 Oct 2020 09:13:18 GMT
EXPOSE 5432
# Thu, 22 Oct 2020 09:13:19 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7eedf40b1ca3ca0c12781ef9399626d49e7898eb4dc6bf3888a3add86c9ee2`  
		Last Modified: Thu, 22 Oct 2020 09:17:08 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2cc4a27e16f2350721162545664e1c967b92e8a0ecffb90828c979f0bc3ac6`  
		Last Modified: Thu, 22 Oct 2020 09:17:08 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53785c7aec3d1276ae4b10987aa89cebc8412388045f6baf9f0a637bbb0c2015`  
		Last Modified: Thu, 22 Oct 2020 09:18:50 GMT  
		Size: 10.4 MB (10441734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275f309721b4225433fc48686dbe7d6410d89807a0cdb590c1dcd5649eb484b1`  
		Last Modified: Thu, 22 Oct 2020 09:18:45 GMT  
		Size: 7.2 KB (7157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e104ff37806c9fa3e5008bf545d74a33d4173f8f1579cd4928a496061498d75`  
		Last Modified: Thu, 22 Oct 2020 09:18:45 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801ac3ef86690c912755d74e1c57ed17cc5c73ff9902db3609a9962433db2271`  
		Last Modified: Thu, 22 Oct 2020 09:18:45 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776c133a7d49e198bdd8340af20aa1857a53282f73a6f5db01dbce12364b3d0c`  
		Last Modified: Thu, 22 Oct 2020 09:18:45 GMT  
		Size: 4.3 KB (4259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb08348cca9112313ea90413d551cb1251ef4e9beca2c9aed2e728c9cf090441`  
		Last Modified: Thu, 22 Oct 2020 09:18:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:2d9b40372db5fe833205819860b9a336edef23f5592dc26768f8cb841e66c4b6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14116758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618f1d3c59515af40d2e7ec530ea2e41f81e2cbce49813b5ba350112cf4879dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 08:21:49 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 22 Oct 2020 08:21:49 GMT
ENV LANG=en_US.utf8
# Thu, 22 Oct 2020 08:21:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Oct 2020 08:37:21 GMT
ENV PG_MAJOR=9.6
# Thu, 22 Oct 2020 08:37:22 GMT
ENV PG_VERSION=9.6.19
# Thu, 22 Oct 2020 08:37:22 GMT
ENV PG_SHA256=61f93a94ccddbe0b2d1afaf03f04ba605d8af5b774ff9b830e5adeb50ab55cb0
# Thu, 22 Oct 2020 08:39:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 22 Oct 2020 08:39:53 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 22 Oct 2020 08:39:57 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 22 Oct 2020 08:39:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 Oct 2020 08:40:00 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 22 Oct 2020 08:40:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Oct 2020 08:40:02 GMT
COPY file:be0996fe6c3fcec9976408f3f94ed203fdcb751cfa2cd940a2bfcbbbda925e9c in /usr/local/bin/ 
# Thu, 22 Oct 2020 08:40:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 22 Oct 2020 08:40:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 08:40:07 GMT
STOPSIGNAL SIGINT
# Thu, 22 Oct 2020 08:40:08 GMT
EXPOSE 5432
# Thu, 22 Oct 2020 08:40:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46b3b77440641e62ecc741cdb44f0f558d15c3f3b6d506be26f8c285f7a36ff`  
		Last Modified: Thu, 22 Oct 2020 08:44:00 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85615d5b5e22de086f665265885eae6f4cb41a63e5ed6910df6d0d03d0e90c5`  
		Last Modified: Thu, 22 Oct 2020 08:43:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8141e5be2f31b8d09929acb70098043a5aa98c1f8c86986948c37a843aaa83`  
		Last Modified: Thu, 22 Oct 2020 08:45:38 GMT  
		Size: 11.4 MB (11396878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07261327025c61b6beb447d094d66a06ed88625319d7f4c902a89cadb0d6ae8a`  
		Last Modified: Thu, 22 Oct 2020 08:45:32 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da07d01698a33c72f1fb08fed9b243a446be5275b69c1ad78a06c6890d6fd25`  
		Last Modified: Thu, 22 Oct 2020 08:45:32 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95aad8041870a4e76dc5a00453f1363fe25758d2a41b8c93be7fdc704bf5103d`  
		Last Modified: Thu, 22 Oct 2020 08:45:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b21e61063dd7b2895ff5df47faff52baf9b388034c7ed66e0340f88b9a2dbc`  
		Last Modified: Thu, 22 Oct 2020 08:45:32 GMT  
		Size: 4.3 KB (4262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236756de9b740bc6ee28fb6b31caf2526a4111f3ebee1eac2def95f6b0efc012`  
		Last Modified: Thu, 22 Oct 2020 08:45:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; 386

```console
$ docker pull postgres@sha256:1ed451a975f14d9b179c34833299ad2f2ff912b1399e5e4fda9c0673928b85af
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14989304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac0655a0cd9bce8a679dfb01a2b0b62cda2d77d22872a3c735e020d06366ac3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 09:38:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 22 Oct 2020 09:38:39 GMT
ENV LANG=en_US.utf8
# Thu, 22 Oct 2020 09:38:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Oct 2020 10:10:53 GMT
ENV PG_MAJOR=9.6
# Thu, 22 Oct 2020 10:10:53 GMT
ENV PG_VERSION=9.6.19
# Thu, 22 Oct 2020 10:10:53 GMT
ENV PG_SHA256=61f93a94ccddbe0b2d1afaf03f04ba605d8af5b774ff9b830e5adeb50ab55cb0
# Thu, 22 Oct 2020 10:15:35 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 22 Oct 2020 10:15:36 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 22 Oct 2020 10:15:37 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 22 Oct 2020 10:15:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 Oct 2020 10:15:38 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 22 Oct 2020 10:15:38 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Oct 2020 10:15:39 GMT
COPY file:be0996fe6c3fcec9976408f3f94ed203fdcb751cfa2cd940a2bfcbbbda925e9c in /usr/local/bin/ 
# Thu, 22 Oct 2020 10:15:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 22 Oct 2020 10:15:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 10:15:40 GMT
STOPSIGNAL SIGINT
# Thu, 22 Oct 2020 10:15:40 GMT
EXPOSE 5432
# Thu, 22 Oct 2020 10:15:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596122efb908f979efd1794c09ae9c7a15ac0e4d53f2c181fd646d9f32565d9a`  
		Last Modified: Thu, 22 Oct 2020 10:20:51 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feeb7bd791d51cd161cadd22b53bd066e70998ebd55dd5ba92760d35f1ab9e8b`  
		Last Modified: Thu, 22 Oct 2020 10:20:51 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1758be1146af620a798e2b4c53cd74aaf548ebe165a0a08c3fac63ffa4e86b09`  
		Last Modified: Thu, 22 Oct 2020 10:22:33 GMT  
		Size: 12.2 MB (12184704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9d90a4e11d391abfa55d9335c7ec9324a543f2163ff8a1cc125b11a2e4ef97`  
		Last Modified: Thu, 22 Oct 2020 10:22:28 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa48291f0d77a0bd7e9dabdf838169179cfdc6c23857b311fa031163511c4561`  
		Last Modified: Thu, 22 Oct 2020 10:22:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd1293de77bf81d3848e5cbeeda29c1f51f8f928b1f6f1d3717abac98747855a`  
		Last Modified: Thu, 22 Oct 2020 10:22:28 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7dc00f7541cb05ae4ec43b8a95d096076e6429c39978c86850d01ca7c00073`  
		Last Modified: Thu, 22 Oct 2020 10:22:28 GMT  
		Size: 4.3 KB (4258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6da5edf25e93eb293d0dc607c9a1c01b56bb4f23309a332a5d9da92f3c6171`  
		Last Modified: Thu, 22 Oct 2020 10:22:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:a5a6dca3954a8abccc03e64d6d7de5712eba6ceaac3ce394fd9f1fd3db52f896
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15310690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37913a6c66d331d6fd59e0f0ef8f4604700f2a6be84e7d4faf27948f2b494c1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 23:06:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 22 Oct 2020 23:06:17 GMT
ENV LANG=en_US.utf8
# Thu, 22 Oct 2020 23:06:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Oct 2020 23:32:11 GMT
ENV PG_MAJOR=9.6
# Thu, 22 Oct 2020 23:32:20 GMT
ENV PG_VERSION=9.6.19
# Thu, 22 Oct 2020 23:32:27 GMT
ENV PG_SHA256=61f93a94ccddbe0b2d1afaf03f04ba605d8af5b774ff9b830e5adeb50ab55cb0
# Thu, 22 Oct 2020 23:35:05 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 22 Oct 2020 23:35:18 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 22 Oct 2020 23:35:31 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 22 Oct 2020 23:35:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 Oct 2020 23:35:54 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 22 Oct 2020 23:35:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Oct 2020 23:35:59 GMT
COPY file:be0996fe6c3fcec9976408f3f94ed203fdcb751cfa2cd940a2bfcbbbda925e9c in /usr/local/bin/ 
# Thu, 22 Oct 2020 23:36:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 22 Oct 2020 23:36:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 23:36:20 GMT
STOPSIGNAL SIGINT
# Thu, 22 Oct 2020 23:36:25 GMT
EXPOSE 5432
# Thu, 22 Oct 2020 23:36:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40cba28bb2e7e5449306ade2eb73dd95379370b59f2eac45aa9f62aa4d376b1`  
		Last Modified: Thu, 22 Oct 2020 23:41:44 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b145001d871735701a01931a308a05fafba12a34115cac00163359d3ed8cf19`  
		Last Modified: Thu, 22 Oct 2020 23:41:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6a1a73ecd917bb30acaba74aa897d40dd155ce8c61f25c6093ebbe34a9b014`  
		Last Modified: Thu, 22 Oct 2020 23:43:59 GMT  
		Size: 12.5 MB (12494146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6f70e06b6dc89317aaec50adfd52d8f2ee7f88fe47fcbf68a5adec7c98fdad`  
		Last Modified: Thu, 22 Oct 2020 23:43:51 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d353780080303b0aaa6521d28febb7c2c906191e6a2a6ddee9b381d5298a6c4e`  
		Last Modified: Thu, 22 Oct 2020 23:43:51 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c44ecf52e8a38cedb46f2db89186752750dca720c5aa2cfa5951a8578cc81`  
		Last Modified: Thu, 22 Oct 2020 23:43:50 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cf1ed629be8e282f7a83ad8c9be39033c366b806180dc40ce47368d50b1b21`  
		Last Modified: Thu, 22 Oct 2020 23:43:51 GMT  
		Size: 4.3 KB (4264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ff792e55d1b8e76fb093b3f0c59408466b080ca2e637bd47c9e8e1c4c7a984`  
		Last Modified: Thu, 22 Oct 2020 23:43:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:043bc5a0988b5d70581f6eaf28fb4179d09924b943833a41e599e99de93d1e8e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13947828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c0a66df00471b6b7de7c17c3de326a3ebb3154f1a837ea476d1bae51d1d082`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 22 Oct 2020 01:59:08 GMT
ADD file:e07d6f40b1afc3d3eff230bc89e84704eb762706a373a60c6bea6a45b2287464 in / 
# Thu, 22 Oct 2020 01:59:09 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 09:05:49 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 22 Oct 2020 09:05:49 GMT
ENV LANG=en_US.utf8
# Thu, 22 Oct 2020 09:05:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Oct 2020 09:23:07 GMT
ENV PG_MAJOR=9.6
# Thu, 22 Oct 2020 09:23:08 GMT
ENV PG_VERSION=9.6.19
# Thu, 22 Oct 2020 09:23:09 GMT
ENV PG_SHA256=61f93a94ccddbe0b2d1afaf03f04ba605d8af5b774ff9b830e5adeb50ab55cb0
# Thu, 22 Oct 2020 09:25:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 22 Oct 2020 09:25:41 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 22 Oct 2020 09:25:42 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 22 Oct 2020 09:25:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 Oct 2020 09:25:44 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 22 Oct 2020 09:25:45 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Oct 2020 09:25:45 GMT
COPY file:be0996fe6c3fcec9976408f3f94ed203fdcb751cfa2cd940a2bfcbbbda925e9c in /usr/local/bin/ 
# Thu, 22 Oct 2020 09:25:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 22 Oct 2020 09:25:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 09:25:48 GMT
STOPSIGNAL SIGINT
# Thu, 22 Oct 2020 09:25:49 GMT
EXPOSE 5432
# Thu, 22 Oct 2020 09:25:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a4c84ece3d2b98927d25f13a4f367bfd96cbfae272f6ff1117d74c84b92d11d3`  
		Last Modified: Thu, 22 Oct 2020 01:59:37 GMT  
		Size: 2.6 MB (2565829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4788b366e4c5d5f3b69b31ae06b2811fe54eb39bd4fd8b6107985f9982ab150a`  
		Last Modified: Thu, 22 Oct 2020 09:29:06 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eed686015d5efd53e62cc5b3f61833711a48184edf03c7d21f021b34f23095`  
		Last Modified: Thu, 22 Oct 2020 09:29:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2502469121171c05fc2f76e2ad25767cecbc16ec44c84033ab905b36752eb0d`  
		Last Modified: Thu, 22 Oct 2020 09:30:42 GMT  
		Size: 11.4 MB (11368676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33cc3be8653ac381149a46e7f166fde6a9ca653af9910e5f3d5a35264a36f29a`  
		Last Modified: Thu, 22 Oct 2020 09:30:38 GMT  
		Size: 7.2 KB (7156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b285cd8c68c9ee9e6f882198a1940aa45563fe88a8146469b79631151b7efbf`  
		Last Modified: Thu, 22 Oct 2020 09:30:38 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502a91a7c371d7662208ddf836152fadf3edeff45575861591c96ca9f5208a8b`  
		Last Modified: Thu, 22 Oct 2020 09:30:38 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368653c8a2e4b08c6667d3e0a3655086f876d2b4ff5010959422ab2abfb4309`  
		Last Modified: Thu, 22 Oct 2020 09:30:38 GMT  
		Size: 4.3 KB (4265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e262a0e2bb6bc8b64f64f8fe85e555c43914c92b037beb969cb3bd3117995696`  
		Last Modified: Thu, 22 Oct 2020 09:30:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
