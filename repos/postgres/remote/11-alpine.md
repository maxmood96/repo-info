## `postgres:11-alpine`

```console
$ docker pull postgres@sha256:2f195f66485015abbe0853fbb0da85603f40d9111f14278487c075d3a9f93084
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

### `postgres:11-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:7eb2962f883f1d984a8938c135cb432c47a33f5184b7d3f87bed8f67d53449df
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60542704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1e25ef56d1e2a3b0077357e198db6dc1f5552f09a95937dbfc1379d478dfe9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:44:32 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 15 Apr 2021 03:44:32 GMT
ENV LANG=en_US.utf8
# Thu, 15 Apr 2021 03:44:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 15 Apr 2021 03:59:20 GMT
ENV PG_MAJOR=11
# Thu, 15 Apr 2021 03:59:21 GMT
ENV PG_VERSION=11.11
# Thu, 15 Apr 2021 03:59:21 GMT
ENV PG_SHA256=40607b7fa15b7d63f5075a7277daf7b3412486aa5db3aedffdb7768b9298186c
# Thu, 15 Apr 2021 04:06:29 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Apr 2021 04:06:31 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Apr 2021 04:06:32 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 15 Apr 2021 04:06:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Apr 2021 04:06:33 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 15 Apr 2021 04:06:33 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Apr 2021 04:06:33 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 15 Apr 2021 04:06:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 15 Apr 2021 04:06:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 04:06:35 GMT
STOPSIGNAL SIGINT
# Thu, 15 Apr 2021 04:06:35 GMT
EXPOSE 5432
# Thu, 15 Apr 2021 04:06:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cb73039552ea36b22e7ea1fabf738b87f83b2c9347901ce77b79c790389bb7`  
		Last Modified: Thu, 15 Apr 2021 04:21:20 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39855706e49a3eeebf4c28a2ff3d706c5cdbe7bb1726d272188f08e91a46bfb8`  
		Last Modified: Thu, 15 Apr 2021 04:21:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71553cacf6c5d050518b2beedfbf948653687f40af086c55bf96db8c4b85dc83`  
		Last Modified: Thu, 15 Apr 2021 04:22:21 GMT  
		Size: 57.7 MB (57716853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74391ac460bbb66629c0b9fdaeed5cb8a6afff37993c3ae59d0bfc0b3f7f98b`  
		Last Modified: Thu, 15 Apr 2021 04:22:10 GMT  
		Size: 7.6 KB (7572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f3d9ec56e6757b05b6d0f8c27f7ab6fd0aceb9c4f8ac5f6437c5cf8e151ee3`  
		Last Modified: Thu, 15 Apr 2021 04:22:09 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8f64be1896392f2f07ed9fe90904fa52254b6e8a46f698547c1a7833b7084b`  
		Last Modified: Thu, 15 Apr 2021 04:22:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b29fd570404e60d637f263b50ef56acde00c17335c7c51dc82c0d82d2a9d71b`  
		Last Modified: Thu, 15 Apr 2021 04:22:08 GMT  
		Size: 4.4 KB (4407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebc7224b03efb9bb0065f66b4872d2dfd026143bfd2f81e601e9eb05194c6f`  
		Last Modified: Thu, 15 Apr 2021 04:22:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:6c41b2a32e15857631e881f9ffca592ebb5406f7bb898d3e3787c87ef59a57b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58871561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e70b1652704e8751f2b8f1fc5c312302c25c96f7c4362bd97d4d2582818ce8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 02:39:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 15 Apr 2021 02:39:45 GMT
ENV LANG=en_US.utf8
# Thu, 15 Apr 2021 02:39:48 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 15 Apr 2021 02:53:06 GMT
ENV PG_MAJOR=11
# Thu, 15 Apr 2021 02:53:06 GMT
ENV PG_VERSION=11.11
# Thu, 15 Apr 2021 02:53:07 GMT
ENV PG_SHA256=40607b7fa15b7d63f5075a7277daf7b3412486aa5db3aedffdb7768b9298186c
# Thu, 15 Apr 2021 02:57:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Apr 2021 02:58:05 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Apr 2021 02:58:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 15 Apr 2021 02:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Apr 2021 02:58:18 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 15 Apr 2021 02:58:19 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Apr 2021 02:58:21 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 15 Apr 2021 02:58:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 15 Apr 2021 02:58:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 02:58:59 GMT
STOPSIGNAL SIGINT
# Thu, 15 Apr 2021 02:59:02 GMT
EXPOSE 5432
# Thu, 15 Apr 2021 02:59:04 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb015ae0de556d839b1cce178f0d7aac974efbf85f07dae41e1cb18f4704b7f2`  
		Last Modified: Thu, 15 Apr 2021 03:12:23 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce063f2d27607cdd3336512bf1e2cdeb8caa1488efded3002dcaf4c6c267a296`  
		Last Modified: Thu, 15 Apr 2021 03:12:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9553500d1e41a42d79e4d9c37afd25a40d849007e600ff004435211660dca2`  
		Last Modified: Thu, 15 Apr 2021 03:13:32 GMT  
		Size: 56.2 MB (56235548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d657550b7fd677c9796fe18508e05a1a7d62b9809ff97946131dcf90c246a3ad`  
		Last Modified: Thu, 15 Apr 2021 03:13:14 GMT  
		Size: 7.6 KB (7573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d17d57f732061ac812e58a798b30e23c3efa2aa41a826aa3ecb49dad25a95c8`  
		Last Modified: Thu, 15 Apr 2021 03:13:16 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72a8b36bad0b3262e7aaa31ec774ea06284e5f3a50d1dae38168f951139ae81`  
		Last Modified: Thu, 15 Apr 2021 03:13:15 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9fe219feca2fd770ffa18ce792b043517fe37b6c273f83c47c520f263218c9`  
		Last Modified: Thu, 15 Apr 2021 03:13:14 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1cae818931929ef7a0ce9e14725af705c14ab88a3bb1f2fd6e36ccea9b6f42`  
		Last Modified: Thu, 15 Apr 2021 03:13:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:d706b23c20bb63f9408281e35beef25c6c01ddcd4712bf50101595bc9cfa9c8a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (55980509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1efc4a8572cab2d44169fc62517542a8f81cf8b6525966bfce89d5e43393501`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:45:28 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 15 Apr 2021 03:45:30 GMT
ENV LANG=en_US.utf8
# Thu, 15 Apr 2021 03:45:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 15 Apr 2021 03:54:31 GMT
ENV PG_MAJOR=11
# Thu, 15 Apr 2021 03:54:32 GMT
ENV PG_VERSION=11.11
# Thu, 15 Apr 2021 03:54:33 GMT
ENV PG_SHA256=40607b7fa15b7d63f5075a7277daf7b3412486aa5db3aedffdb7768b9298186c
# Thu, 15 Apr 2021 03:58:10 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Apr 2021 03:58:18 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Apr 2021 03:58:24 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 15 Apr 2021 03:58:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Apr 2021 03:58:32 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 15 Apr 2021 03:58:34 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Apr 2021 03:58:36 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 15 Apr 2021 03:58:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 15 Apr 2021 03:58:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 03:58:51 GMT
STOPSIGNAL SIGINT
# Thu, 15 Apr 2021 03:58:53 GMT
EXPOSE 5432
# Thu, 15 Apr 2021 03:58:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d289031c7f8e86cc05ec575d7c122bc6d615e827ae76e96bca00fd9b0bba9dfb`  
		Last Modified: Thu, 15 Apr 2021 04:10:49 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b79752b7fbad651a271862e12e829d3ce7258cfa9386e5945f7c4232008d57`  
		Last Modified: Thu, 15 Apr 2021 04:10:49 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b961721583c050f89fbc6cb032a38a0ae2fc99efc7d2e306bfae596ebf5a6572`  
		Last Modified: Thu, 15 Apr 2021 04:11:58 GMT  
		Size: 53.5 MB (53542492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f339b0b9e32a4253e7a6862c463e4b26fd7a4943c6e5fb63cde08feded123980`  
		Last Modified: Thu, 15 Apr 2021 04:11:40 GMT  
		Size: 7.6 KB (7571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b05a5246e144c28296f250415263b1457576f44f1c9e3fa43a9d99de79b924`  
		Last Modified: Thu, 15 Apr 2021 04:11:40 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53976c1f0ad970309fda21eca6584a4c7d971201f329d9a315ba5ad0ff851a6`  
		Last Modified: Thu, 15 Apr 2021 04:11:40 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eb65da14c1fd7cd2e93061b4b0e6967c8c9ac1691ab0dcba9caa9fef8640b2`  
		Last Modified: Thu, 15 Apr 2021 04:11:42 GMT  
		Size: 4.4 KB (4405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d33941a4df2c8b368d5a2897814a7c01db5f5173cb36678a14ea70182cb4ec4`  
		Last Modified: Thu, 15 Apr 2021 04:11:40 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:b4a1e98b01a9b1203c7d33d7b64c64acf35730e42d053f5ceeb97b477f1f16a0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59838096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3d4eb557558578e20db1baa73b002a07e820816d1a6e170a82b4569a24e642`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 15:34:32 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 01 Apr 2021 15:34:33 GMT
ENV LANG=en_US.utf8
# Thu, 01 Apr 2021 15:34:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 01 Apr 2021 15:42:53 GMT
ENV PG_MAJOR=11
# Thu, 01 Apr 2021 15:42:54 GMT
ENV PG_VERSION=11.11
# Thu, 01 Apr 2021 15:42:55 GMT
ENV PG_SHA256=40607b7fa15b7d63f5075a7277daf7b3412486aa5db3aedffdb7768b9298186c
# Thu, 01 Apr 2021 15:46:22 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 01 Apr 2021 15:46:26 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 01 Apr 2021 15:46:28 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 01 Apr 2021 15:46:29 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 01 Apr 2021 15:46:31 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 01 Apr 2021 15:46:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 01 Apr 2021 15:46:33 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 01 Apr 2021 15:46:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 01 Apr 2021 15:46:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 15:46:37 GMT
STOPSIGNAL SIGINT
# Thu, 01 Apr 2021 15:46:38 GMT
EXPOSE 5432
# Thu, 01 Apr 2021 15:46:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4dca3142c84013c57ea8b52a2f4eaa1e53cdce28775ef34cbd2ddaa4a1cc05`  
		Last Modified: Thu, 01 Apr 2021 15:57:51 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f81a7d11e07a928a969377701dbc21b8602aac636b711973d628e633ecbe1a`  
		Last Modified: Thu, 01 Apr 2021 15:57:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b502f8f6cd7788feeff1ce0eb99a0d6d3ff832eabc6233cff5a7dd04d6edbf34`  
		Last Modified: Thu, 01 Apr 2021 15:59:02 GMT  
		Size: 57.1 MB (57112291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c7926143ff23567b05846119ac82136d4cef33c1951a21a2b9ebe9afe72f8d`  
		Last Modified: Thu, 01 Apr 2021 15:58:46 GMT  
		Size: 7.6 KB (7573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e2dc08f11430bdebcb5377f1b06afbccf0e987c39dc36b454f72b777e2ea44`  
		Last Modified: Thu, 01 Apr 2021 15:58:47 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95069b13417c23cd82fb54bc1909cba64d7b8ec815a11832969243ba7d8423b`  
		Last Modified: Thu, 01 Apr 2021 15:58:46 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ddc786ef65c5ed85a91f600853e7e0295c67f998ddb2ade5fc0147ca214a685`  
		Last Modified: Thu, 01 Apr 2021 15:58:46 GMT  
		Size: 4.4 KB (4408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77efdf0e927f9f8f695afb1dfb04e88c344213d4f5a9c9dc7c2fbbe5210d57ef`  
		Last Modified: Thu, 01 Apr 2021 15:58:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; 386

```console
$ docker pull postgres@sha256:25734e5a32864930a40303730b6207ef5a9393a17c91215f2815f7883cbd7543
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63981882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76889b2330def566d1de4e466ce73826176fa153309159a5241cadf19e4c5c03`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 31 Mar 2021 17:43:00 GMT
ADD file:245767f958e2b5e6fad41d45d3361849e7c6b2255303e3c785f0f2c86019553a in / 
# Wed, 31 Mar 2021 17:43:00 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 05:30:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 01 Apr 2021 05:30:17 GMT
ENV LANG=en_US.utf8
# Thu, 01 Apr 2021 05:30:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 01 Apr 2021 05:44:25 GMT
ENV PG_MAJOR=11
# Thu, 01 Apr 2021 05:44:26 GMT
ENV PG_VERSION=11.11
# Thu, 01 Apr 2021 05:44:26 GMT
ENV PG_SHA256=40607b7fa15b7d63f5075a7277daf7b3412486aa5db3aedffdb7768b9298186c
# Thu, 01 Apr 2021 05:51:01 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 01 Apr 2021 05:51:02 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 01 Apr 2021 05:51:03 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 01 Apr 2021 05:51:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 01 Apr 2021 05:51:04 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 01 Apr 2021 05:51:04 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 01 Apr 2021 05:51:04 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 01 Apr 2021 05:51:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 01 Apr 2021 05:51:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 05:51:06 GMT
STOPSIGNAL SIGINT
# Thu, 01 Apr 2021 05:51:06 GMT
EXPOSE 5432
# Thu, 01 Apr 2021 05:51:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b22e590ebf70a9a5901c380b07232ef3c07cb13440402934dfdffb8f8721a949`  
		Last Modified: Wed, 31 Mar 2021 17:44:05 GMT  
		Size: 2.8 MB (2818802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a2b068c1bb76272b0315637db84ae4363b9ba40df2261e23d86c98af1424e7`  
		Last Modified: Thu, 01 Apr 2021 06:04:58 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd976245f3039bbee485288603aab3601719ac5fe74d0adad8c6a81dc749c662`  
		Last Modified: Thu, 01 Apr 2021 06:04:58 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae785d15af19f523b57e9d35076d77a6b422f1fbfd26dbab482df8da5f1b7f0f`  
		Last Modified: Thu, 01 Apr 2021 06:06:23 GMT  
		Size: 61.1 MB (61149205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a34510d5964823d61e02295df1e1c6ef0d1c0e4b007e631717241b6e0bf8b2`  
		Last Modified: Thu, 01 Apr 2021 06:06:02 GMT  
		Size: 7.6 KB (7570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39070878022cd208dcd6bdf9391ab0c777123f273e20f1d9880d57f5150f984e`  
		Last Modified: Thu, 01 Apr 2021 06:06:03 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9cc15bdbfb38bcbb671ff6910b7d2ed2f62b2326565a28d7bdfb57cb9c4d8a`  
		Last Modified: Thu, 01 Apr 2021 06:06:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57771970cf7e9e3cc12c601ac7c8186ac321f4ac65833ac6ba80d29f78ce50ca`  
		Last Modified: Thu, 01 Apr 2021 06:06:03 GMT  
		Size: 4.4 KB (4403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ddb149ff5c12f2d70f9d00c0fdd1455d69bb85efe060e377495cf4d67dcd1e0`  
		Last Modified: Thu, 01 Apr 2021 06:06:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:44e838f01f20c87179dec4f076881f6bef4704959363ac490e2541d05c1c97b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62865850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7fc80c9db1c71aa6d432e0f493ebc88a98130316828f0881303bda12d245aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 31 Mar 2021 18:55:41 GMT
ADD file:1dd3315eb685a1b6729efb6f5b634e414f3da0f065078952bc6c0339dc09512d in / 
# Wed, 31 Mar 2021 18:55:49 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 23:54:45 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 01 Apr 2021 23:54:51 GMT
ENV LANG=en_US.utf8
# Thu, 01 Apr 2021 23:55:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 02 Apr 2021 00:10:58 GMT
ENV PG_MAJOR=11
# Fri, 02 Apr 2021 00:11:16 GMT
ENV PG_VERSION=11.11
# Fri, 02 Apr 2021 00:11:28 GMT
ENV PG_SHA256=40607b7fa15b7d63f5075a7277daf7b3412486aa5db3aedffdb7768b9298186c
# Fri, 02 Apr 2021 00:15:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 02 Apr 2021 00:16:13 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 02 Apr 2021 00:16:34 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 02 Apr 2021 00:16:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 02 Apr 2021 00:16:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 02 Apr 2021 00:17:01 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 02 Apr 2021 00:17:04 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Fri, 02 Apr 2021 00:17:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 02 Apr 2021 00:17:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Apr 2021 00:17:41 GMT
STOPSIGNAL SIGINT
# Fri, 02 Apr 2021 00:17:51 GMT
EXPOSE 5432
# Fri, 02 Apr 2021 00:17:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dc4792b25345295bf964e1db1bceedb2338bfad8f0fb64f0cc07b152df9aef84`  
		Last Modified: Wed, 31 Mar 2021 18:57:19 GMT  
		Size: 2.8 MB (2813219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e2ee829b243db77878a7d15d4126a4e817b6216820082d82dfb11cc8756e45`  
		Last Modified: Fri, 02 Apr 2021 00:35:00 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d13418e7dceb873ab132346668dbf070e938bac34b9ec7f0ad08583ed7387b`  
		Last Modified: Fri, 02 Apr 2021 00:35:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266940af354f8973ed1c4acbd81e01946d16c760b0e499d427e30e1cf08b305a`  
		Last Modified: Fri, 02 Apr 2021 00:36:06 GMT  
		Size: 60.0 MB (60038751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fcebfea40de5547637d139a0bd9e71a1f2a8f6daf625fe70ee9cb3544566e7`  
		Last Modified: Fri, 02 Apr 2021 00:35:51 GMT  
		Size: 7.6 KB (7572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2563452bdb89bfba691f7821957dba94f23d4e1deceefdb4746af0c50d95df`  
		Last Modified: Fri, 02 Apr 2021 00:35:51 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2766530c94837f72660b416668543bb94ea4868c5ea4ec58529e6c64abe3d042`  
		Last Modified: Fri, 02 Apr 2021 00:35:51 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbcb527c2eee52eab6cdf5f778934b4a0167168ad089963834b3965dd87e1d58`  
		Last Modified: Fri, 02 Apr 2021 00:35:51 GMT  
		Size: 4.4 KB (4403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d0b1926ddb9624e3bdba6584acca5aec788c7ca03649b84861c3a5acc19c7e`  
		Last Modified: Fri, 02 Apr 2021 00:35:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:11697218a7ee180ede9a9220f46e019fa0f9c5892f8d85a3637166931b167c83
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62836450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6972a73525f10c5e61ca94b4c16024a28faae399dae7e6c52aa60a6a72cf1365`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 02:35:26 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 15 Apr 2021 02:35:26 GMT
ENV LANG=en_US.utf8
# Thu, 15 Apr 2021 02:35:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 15 Apr 2021 02:43:29 GMT
ENV PG_MAJOR=11
# Thu, 15 Apr 2021 02:43:30 GMT
ENV PG_VERSION=11.11
# Thu, 15 Apr 2021 02:43:30 GMT
ENV PG_SHA256=40607b7fa15b7d63f5075a7277daf7b3412486aa5db3aedffdb7768b9298186c
# Thu, 15 Apr 2021 02:47:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Apr 2021 02:47:07 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Apr 2021 02:47:08 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 15 Apr 2021 02:47:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Apr 2021 02:47:09 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 15 Apr 2021 02:47:09 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Apr 2021 02:47:10 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 15 Apr 2021 02:47:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 15 Apr 2021 02:47:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 02:47:11 GMT
STOPSIGNAL SIGINT
# Thu, 15 Apr 2021 02:47:12 GMT
EXPOSE 5432
# Thu, 15 Apr 2021 02:47:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f539beccb9c12dbbd5eb5238188d7421b0e766e3e536f47e5a25dce4187b138f`  
		Last Modified: Thu, 15 Apr 2021 02:55:28 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78639c932051e59362713e29f35ff376c4cd5627ea231422efbf7cf7b253ec7a`  
		Last Modified: Thu, 15 Apr 2021 02:55:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6256fe1451e600c4bc4ec903bbdf5cf8fddef31e3418b1135aa4fadc7531d435`  
		Last Modified: Thu, 15 Apr 2021 02:56:07 GMT  
		Size: 60.2 MB (60219928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49910a65090099f3596f0b19f0779f12f6cc29f1fe313e5be4550d50e4ef8611`  
		Last Modified: Thu, 15 Apr 2021 02:55:57 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c436626a0d06240211961e287390c498e05fdd1d47ebbc25434090b5a2f1ca`  
		Last Modified: Thu, 15 Apr 2021 02:55:57 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d5b818f4da67b37c549a4e71fd10716a93c1e50cc8e8bc0e202dc5843db012`  
		Last Modified: Thu, 15 Apr 2021 02:55:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68491ed26a419d878ed43baaa51e6b30a7070f1057f7ec6e4245295e5f95de62`  
		Last Modified: Thu, 15 Apr 2021 02:55:57 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f5eb0b3399a68c6bca169aee713f90c04a97a34472e05f71e1cb4647afb467`  
		Last Modified: Thu, 15 Apr 2021 02:55:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
