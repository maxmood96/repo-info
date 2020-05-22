## `postgres:13-beta1-alpine`

```console
$ docker pull postgres@sha256:fdd338bfd174949070f3e7edff2bf3fa08e98440fc37316f5393fbc6441f6c38
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

### `postgres:13-beta1-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:d6abc1a9c56523dfd6d2c57d7e1299f437eb5f4ff6dfd24ade244a6cc69134d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60369487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edc8ca392867fbb67bcc475703163206f3a2d9d80fcc19c2123b045b40d7a8c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:11:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 24 Apr 2020 17:11:48 GMT
ENV LANG=en_US.utf8
# Fri, 24 Apr 2020 17:11:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 May 2020 01:30:07 GMT
ENV PG_MAJOR=13
# Fri, 22 May 2020 01:30:07 GMT
ENV PG_VERSION=13beta1
# Fri, 22 May 2020 01:30:07 GMT
ENV PG_SHA256=249ba0d0227d5393b83d397f2543354bfee579276cb1e821e9b7d904a42039e1
# Fri, 22 May 2020 01:36:09 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm9-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Fri, 22 May 2020 01:36:10 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 22 May 2020 01:36:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 22 May 2020 01:36:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 May 2020 01:36:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 22 May 2020 01:36:12 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 May 2020 01:36:12 GMT
COPY file:33e6fc6ab9ea2b87183e496ad72f1df7f682913ffd781b1451fd178b0c7d745a in /usr/local/bin/ 
# Fri, 22 May 2020 01:36:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 May 2020 01:36:13 GMT
EXPOSE 5432
# Fri, 22 May 2020 01:36:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52a8a2ca21a6b2f35ce4b89cf728e4fa7d53206b2a18ab3fa1a285e0bfe4726`  
		Last Modified: Fri, 24 Apr 2020 17:32:23 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36a19831e31f1aa75ef228b7a788b936a99bd97f74d7a6967e4379bd807d680`  
		Last Modified: Fri, 24 Apr 2020 17:32:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ff73dc4a343eaba3c5b5ab9bf3f35a729996c0d5be0f479475808cb017cf03`  
		Last Modified: Fri, 22 May 2020 01:37:38 GMT  
		Size: 57.5 MB (57541722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc46bdee4cd8e20acdea459f64b8e3a11846908940d0a3d4622080442f7b5b77`  
		Last Modified: Fri, 22 May 2020 01:37:28 GMT  
		Size: 8.5 KB (8533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23df77640d114e17e2d0f165cef08c331c2091d2278a597d5e0334a15faeca8c`  
		Last Modified: Fri, 22 May 2020 01:37:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b48cf7023cf8c7e8a3bdcacac95be1e3b4de9381b06b47a441dadb6d5db8b068`  
		Last Modified: Fri, 22 May 2020 01:37:28 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe36e29ac2cd49464f5599709e8c9bfacc3f0b44e879861861127bba5107e00`  
		Last Modified: Fri, 22 May 2020 01:37:28 GMT  
		Size: 4.3 KB (4260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-beta1-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:d20b04885e61744824996e1d513e194b9e37bebb5939bea25de36300103fea79
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58701602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0e2213130039b13b362aca4e46c29079b913f4c53cab9df92efd4b86d0e6b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 19:57:11 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 23 Apr 2020 19:57:12 GMT
ENV LANG=en_US.utf8
# Thu, 23 Apr 2020 19:57:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 May 2020 01:52:44 GMT
ENV PG_MAJOR=13
# Fri, 22 May 2020 01:52:44 GMT
ENV PG_VERSION=13beta1
# Fri, 22 May 2020 01:52:45 GMT
ENV PG_SHA256=249ba0d0227d5393b83d397f2543354bfee579276cb1e821e9b7d904a42039e1
# Fri, 22 May 2020 01:57:03 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm9-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Fri, 22 May 2020 01:57:07 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 22 May 2020 01:57:10 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 22 May 2020 01:57:10 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 May 2020 01:57:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 22 May 2020 01:57:14 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 May 2020 01:57:15 GMT
COPY file:33e6fc6ab9ea2b87183e496ad72f1df7f682913ffd781b1451fd178b0c7d745a in /usr/local/bin/ 
# Fri, 22 May 2020 01:57:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 May 2020 01:57:19 GMT
EXPOSE 5432
# Fri, 22 May 2020 01:57:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0fe18342defa413ae03aef3e0942cb59be0cd23d148c8f00345d83bdd3caf9`  
		Last Modified: Thu, 23 Apr 2020 20:16:50 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd53a6698d4905175d063c44335ca7e40d621093d6a69b00b07a084b41811b6`  
		Last Modified: Thu, 23 Apr 2020 20:16:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a498780c621b6d1566f55d193c2fcff1e578ec24c74316a85b223987b0cf85`  
		Last Modified: Fri, 22 May 2020 01:58:24 GMT  
		Size: 56.1 MB (56067096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c921ab4263d2c681b0ffbb1c2636af765b5026b108a75bca5b2f68a38ec93f1`  
		Last Modified: Fri, 22 May 2020 01:58:07 GMT  
		Size: 8.5 KB (8532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5d40a70111535e16309e1e70c8b300e556d7a31aec98daf2585e226ee2b5e1`  
		Last Modified: Fri, 22 May 2020 01:58:07 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e921229183f57afdd87ce96f7e6e650102bde12cac66edfe8737ccd9f5e780d`  
		Last Modified: Fri, 22 May 2020 01:58:07 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d13e16ce80f576637c32c56b83afc12f6b2297503d5c624f8131d2397dffef6`  
		Last Modified: Fri, 22 May 2020 01:58:07 GMT  
		Size: 4.3 KB (4263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-beta1-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:d4cf668d96cbb982c735fffcbddc0d077df5a468335daaa9ffbe605674738819
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55933235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d327fb7f8fafff25a035b984009cb7a485878f969b66bcbcdd486908aeac783`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 08:33:33 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 24 Apr 2020 08:33:34 GMT
ENV LANG=en_US.utf8
# Fri, 24 Apr 2020 08:33:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 May 2020 01:24:05 GMT
ENV PG_MAJOR=13
# Fri, 22 May 2020 01:24:06 GMT
ENV PG_VERSION=13beta1
# Fri, 22 May 2020 01:24:06 GMT
ENV PG_SHA256=249ba0d0227d5393b83d397f2543354bfee579276cb1e821e9b7d904a42039e1
# Fri, 22 May 2020 01:26:57 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm9-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Fri, 22 May 2020 01:27:00 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 22 May 2020 01:27:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 22 May 2020 01:27:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 May 2020 01:27:09 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 22 May 2020 01:27:10 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 May 2020 01:27:10 GMT
COPY file:33e6fc6ab9ea2b87183e496ad72f1df7f682913ffd781b1451fd178b0c7d745a in /usr/local/bin/ 
# Fri, 22 May 2020 01:27:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 May 2020 01:27:12 GMT
EXPOSE 5432
# Fri, 22 May 2020 01:27:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d4bbcefb265020b323ff09da302c8b4ee3db8f6da7d0de3d3ea655798ff865`  
		Last Modified: Fri, 24 Apr 2020 08:48:13 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e53cbfc4447cbfa4e0f492480f510e5bac84d1397e9f66a8dc7a57186a7772`  
		Last Modified: Fri, 24 Apr 2020 08:48:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8ff333122eec74e9d987e9c8fed47e7b78e7e38c445513cf8de1bc1b50f81d`  
		Last Modified: Fri, 22 May 2020 01:29:11 GMT  
		Size: 53.5 MB (53496595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a60343abf728752a79d38a37df24407e128551a88d55a3f7554532f3c46d83e`  
		Last Modified: Fri, 22 May 2020 01:28:57 GMT  
		Size: 8.5 KB (8531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a4601ea5319ccdd774bc4c34c5911d503f5dbc4bac5efae403191ac39d5098`  
		Last Modified: Fri, 22 May 2020 01:28:57 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e86ab1ce6825df0184d1cf438550e7fd7eb7d7d32853c6541f4d1b564e5ad0`  
		Last Modified: Fri, 22 May 2020 01:28:57 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c129a35160e7f59b6200e3be3aefb59fa22615de3c0cf57e67e412825a78ec62`  
		Last Modified: Fri, 22 May 2020 01:28:57 GMT  
		Size: 4.3 KB (4264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-beta1-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:f12d7b6c1d5bdb847a80d1d57080b708ea16d5d3e3d8731d53c92450c98a0386
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59922380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c1eba2ec1e557fe962e50291f91655a8357abb511b20434322b5066d810015`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:08:36 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 24 Apr 2020 14:08:38 GMT
ENV LANG=en_US.utf8
# Fri, 24 Apr 2020 14:08:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 May 2020 01:53:01 GMT
ENV PG_MAJOR=13
# Fri, 22 May 2020 01:53:02 GMT
ENV PG_VERSION=13beta1
# Fri, 22 May 2020 01:53:04 GMT
ENV PG_SHA256=249ba0d0227d5393b83d397f2543354bfee579276cb1e821e9b7d904a42039e1
# Fri, 22 May 2020 01:57:04 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm9-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Fri, 22 May 2020 01:57:08 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 22 May 2020 01:57:10 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 22 May 2020 01:57:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 May 2020 01:57:14 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 22 May 2020 01:57:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 May 2020 01:57:17 GMT
COPY file:33e6fc6ab9ea2b87183e496ad72f1df7f682913ffd781b1451fd178b0c7d745a in /usr/local/bin/ 
# Fri, 22 May 2020 01:57:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 May 2020 01:57:20 GMT
EXPOSE 5432
# Fri, 22 May 2020 01:57:21 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2deb5bf01f13e32487d25d3e9a01a520f37169eb3947129cd16b8cf850d5bab`  
		Last Modified: Fri, 24 Apr 2020 14:25:41 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d56ad23dde28bb28a0df49e642e38f043a63a0c8d44cf228044eff1827de50`  
		Last Modified: Fri, 24 Apr 2020 14:25:41 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda747fb225b0242675339fbb7e63aff2a995bd95802fb9ef71ec51cf14ac995`  
		Last Modified: Fri, 22 May 2020 01:59:17 GMT  
		Size: 57.2 MB (57183377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152826d6b774cf71cab7090e534ca20abdfe014540a99da5fb863f1f33fbc945`  
		Last Modified: Fri, 22 May 2020 01:59:00 GMT  
		Size: 8.5 KB (8536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5d40a70111535e16309e1e70c8b300e556d7a31aec98daf2585e226ee2b5e1`  
		Last Modified: Fri, 22 May 2020 01:58:07 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98a05bb12f84e6da2da5db55895fa9e8095017a056ba38fba6c518de73e6afe`  
		Last Modified: Fri, 22 May 2020 01:59:00 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7962af390b7c7502f7a9b6eb05b4ada68533c27b8c9e31a874de21822612611c`  
		Last Modified: Fri, 22 May 2020 01:59:00 GMT  
		Size: 4.3 KB (4261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-beta1-alpine` - linux; 386

```console
$ docker pull postgres@sha256:a93384dc1661b1b62804bf881ffdd6bf5a18489a2d19eb66701419290cacdb3f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63697153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c3172123c9542ebfa233c4052083fa89567ca94193c77b99f6cfd8ab7316e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:04 GMT
ADD file:63bd8a316cba8c404cc2e32a5120406c24aee8db3224c469a6077b941d900863 in / 
# Thu, 23 Apr 2020 21:16:04 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 08:04:33 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 24 Apr 2020 08:04:33 GMT
ENV LANG=en_US.utf8
# Fri, 24 Apr 2020 08:04:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 May 2020 01:40:57 GMT
ENV PG_MAJOR=13
# Fri, 22 May 2020 01:40:58 GMT
ENV PG_VERSION=13beta1
# Fri, 22 May 2020 01:40:58 GMT
ENV PG_SHA256=249ba0d0227d5393b83d397f2543354bfee579276cb1e821e9b7d904a42039e1
# Fri, 22 May 2020 01:47:57 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm9-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Fri, 22 May 2020 01:47:58 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 22 May 2020 01:47:58 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 22 May 2020 01:47:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 May 2020 01:48:00 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 22 May 2020 01:48:00 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 May 2020 01:48:00 GMT
COPY file:33e6fc6ab9ea2b87183e496ad72f1df7f682913ffd781b1451fd178b0c7d745a in /usr/local/bin/ 
# Fri, 22 May 2020 01:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 May 2020 01:48:00 GMT
EXPOSE 5432
# Fri, 22 May 2020 01:48:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40ec1727ae78424ec003d6b3506985950e6d173ecedacfc6d96b4803ec3fd24`  
		Last Modified: Fri, 24 Apr 2020 08:32:09 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adaab1850ecb85cd8d44baa5bb4784f13183b1419bc09a56384105985dd11a45`  
		Last Modified: Fri, 24 Apr 2020 08:32:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2889b9dea02de8c7a44ceae2df4b4679acff042ae0cc5995efea0a5f9787d43e`  
		Last Modified: Fri, 22 May 2020 01:49:37 GMT  
		Size: 60.9 MB (60874288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a509cb2e6746621763d1f4d397a38b718752a2ece3cdbbf4af7c14335fd2a51`  
		Last Modified: Fri, 22 May 2020 01:49:24 GMT  
		Size: 8.5 KB (8531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16d93e16792e043cb6388147a2b1e91309ed791e92cf0f2a31cf045ed8be9c8`  
		Last Modified: Fri, 22 May 2020 01:49:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad737f89958776912642bed5201a4c88a38d61d4a294253c1b295fbaaf14076`  
		Last Modified: Fri, 22 May 2020 01:49:24 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4570e72c184f05560e2f7ebbf38a3650814febd5d7bfaec89f1a4804b91c9a1b`  
		Last Modified: Fri, 22 May 2020 01:49:25 GMT  
		Size: 4.3 KB (4260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-beta1-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:311c2db638ff310a5dcdca5a5ea425c9c8b155b2ac18eaf0e5cb33111256545b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62638424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:890fa5a3cd1cfae6ab7afedbbe6aca1eb4aa9ff9445782ef8de7edaf9643bdb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 06:26:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 24 Apr 2020 06:26:26 GMT
ENV LANG=en_US.utf8
# Fri, 24 Apr 2020 06:26:37 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 May 2020 01:23:32 GMT
ENV PG_MAJOR=13
# Fri, 22 May 2020 01:23:38 GMT
ENV PG_VERSION=13beta1
# Fri, 22 May 2020 01:23:49 GMT
ENV PG_SHA256=249ba0d0227d5393b83d397f2543354bfee579276cb1e821e9b7d904a42039e1
# Fri, 22 May 2020 01:29:44 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm9-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Fri, 22 May 2020 01:30:04 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 22 May 2020 01:30:14 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 22 May 2020 01:30:19 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 May 2020 01:30:28 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 22 May 2020 01:30:32 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 May 2020 01:30:38 GMT
COPY file:33e6fc6ab9ea2b87183e496ad72f1df7f682913ffd781b1451fd178b0c7d745a in /usr/local/bin/ 
# Fri, 22 May 2020 01:30:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 May 2020 01:30:46 GMT
EXPOSE 5432
# Fri, 22 May 2020 01:30:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8df1307f81687eb57717789c618ebcae3d1f81c5c155bdd5b96e38d71bb9747`  
		Last Modified: Fri, 24 Apr 2020 06:55:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c05d9c9ea5c9eb70234c2443b1e0a454ba2f750d808560d28fa8ed32229167`  
		Last Modified: Fri, 24 Apr 2020 06:55:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071149f947005476357d5f7db2bc24d269caa22b6903e8e20b389ebc6109d4bc`  
		Last Modified: Fri, 22 May 2020 01:33:20 GMT  
		Size: 59.8 MB (59801993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c7c07afc9c7e75e10e85e0b7b14535a88f6afe5ae61b497ab4fb9ff77c5288`  
		Last Modified: Fri, 22 May 2020 01:33:08 GMT  
		Size: 8.5 KB (8536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54adc57c4a3a52b893586d69e4437785e3fa86547f93256306c406a1b74ecf`  
		Last Modified: Fri, 22 May 2020 01:33:08 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b55415e7b38e271300eaa3a663219d88c0a8aa50b4d2702fa6ce65805970d11`  
		Last Modified: Fri, 22 May 2020 01:33:08 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf30038929fe85f4f8e32d36902e175b241a4ea2d8f39f1fdb9e94da829980ee`  
		Last Modified: Fri, 22 May 2020 01:33:08 GMT  
		Size: 4.3 KB (4260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-beta1-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:f7088593c0b739eca04c915b967f9d6e034ce020753f0e9cb9971e37462290ab
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62774032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4cd70fb4159a6ac9293e6e95e8e811870f789e25895511e24934856d17e35db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 06:45:36 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 24 Apr 2020 06:45:36 GMT
ENV LANG=en_US.utf8
# Fri, 24 Apr 2020 06:45:37 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 22 May 2020 01:50:53 GMT
ENV PG_MAJOR=13
# Fri, 22 May 2020 01:50:53 GMT
ENV PG_VERSION=13beta1
# Fri, 22 May 2020 01:50:53 GMT
ENV PG_SHA256=249ba0d0227d5393b83d397f2543354bfee579276cb1e821e9b7d904a42039e1
# Fri, 22 May 2020 01:54:34 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm9-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Fri, 22 May 2020 01:54:37 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 22 May 2020 01:54:37 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 22 May 2020 01:54:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 May 2020 01:54:38 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 22 May 2020 01:54:39 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 May 2020 01:54:39 GMT
COPY file:33e6fc6ab9ea2b87183e496ad72f1df7f682913ffd781b1451fd178b0c7d745a in /usr/local/bin/ 
# Fri, 22 May 2020 01:54:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 May 2020 01:54:39 GMT
EXPOSE 5432
# Fri, 22 May 2020 01:54:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fde159b9a8b82bd8df9811d19510149c4b99ee867783653adaab28baa4143ae`  
		Last Modified: Fri, 24 Apr 2020 07:01:01 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7825d6effaa586d60a176215d9f11ecd1bd76c6afe3e47f50f6259ad464598b3`  
		Last Modified: Fri, 24 Apr 2020 07:00:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b33037c4df52b5f1c70c120ed4556e5695e413444ac4b1164d4d10a3a5eff5a`  
		Last Modified: Fri, 22 May 2020 01:56:17 GMT  
		Size: 60.2 MB (60176599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdfdb63922d7943e5f9e8b041dfbe21482d30601e87180c71400a48cc7ab4ef`  
		Last Modified: Fri, 22 May 2020 01:56:09 GMT  
		Size: 8.5 KB (8530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f797813e7de782f438b3500286dfa065c68f91edac18e7bd54b7cc785454ff4`  
		Last Modified: Fri, 22 May 2020 01:56:25 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb568f6f9cbf20245dbe100b1e88713e0c3be6cdc3c8a5179615067d6b5ac4ff`  
		Last Modified: Fri, 22 May 2020 01:56:25 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7734f1e2155daff1b74dd9adf24b9810e1ffc80ce421f4e69689e2a3ba0a54`  
		Last Modified: Fri, 22 May 2020 01:56:25 GMT  
		Size: 4.3 KB (4263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
