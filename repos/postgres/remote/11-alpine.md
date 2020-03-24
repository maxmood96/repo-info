## `postgres:11-alpine`

```console
$ docker pull postgres@sha256:fdecfb9a2de3bd27ca695cecb79b4519b74f7c9e505fa4f9129a9e72e8ff5193
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
$ docker pull postgres@sha256:785334846c220affdc714ecf06fab5006c96dbe2cef6ecd9860f21f330b5caeb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58793523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3c792d447476ee61f2fcf08e9af3e4d3017ce10085e28942e1f8442b718068`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:47:57 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Mon, 23 Mar 2020 23:47:57 GMT
ENV LANG=en_US.utf8
# Mon, 23 Mar 2020 23:47:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 23 Mar 2020 23:58:22 GMT
ENV PG_MAJOR=11
# Mon, 23 Mar 2020 23:58:22 GMT
ENV PG_VERSION=11.7
# Mon, 23 Mar 2020 23:58:23 GMT
ENV PG_SHA256=324ae93a8846fbb6a25d562d271bc441ffa8794654c5b2839384834de220a313
# Tue, 24 Mar 2020 00:09:11 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm9-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Tue, 24 Mar 2020 00:09:12 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 24 Mar 2020 00:09:14 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 24 Mar 2020 00:09:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 24 Mar 2020 00:09:16 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 24 Mar 2020 00:09:16 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 24 Mar 2020 00:09:17 GMT
COPY file:33e6fc6ab9ea2b87183e496ad72f1df7f682913ffd781b1451fd178b0c7d745a in /usr/local/bin/ 
# Tue, 24 Mar 2020 00:09:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 24 Mar 2020 00:09:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2020 00:09:19 GMT
EXPOSE 5432
# Tue, 24 Mar 2020 00:09:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b4c973b808455b5a0f405abb1ae54c769bf4a42a7af686fc96b4469b3444e5`  
		Last Modified: Tue, 24 Mar 2020 00:28:16 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074a034a3a7aef9e887181bce1bf5fcf938f0c6d5ac8929d6139853efa4c850b`  
		Last Modified: Tue, 24 Mar 2020 00:28:16 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9baafdb78901c05a379f58d989c9a3a1ce68592803d9703583da15a26c9b4f98`  
		Last Modified: Tue, 24 Mar 2020 00:28:54 GMT  
		Size: 56.0 MB (55976658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3d6dccc83df24e9b4ee215a6052b5b6e2ea512843a004c5aba1aea1e2a794e`  
		Last Modified: Tue, 24 Mar 2020 00:28:39 GMT  
		Size: 7.6 KB (7575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbeeb53f7511d02c9d45001f8a71f73ab201cfe8c3e00998953dd23260ae5bfa`  
		Last Modified: Tue, 24 Mar 2020 00:28:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d3687f9b22c98f9c11b6e8b63d890e19dff0004706d8f441d1b9dad0b9fe7a`  
		Last Modified: Tue, 24 Mar 2020 00:28:38 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9d21a2c9999dda52030a5176635048b8b8b4fdb4794490dd18f219ca684518`  
		Last Modified: Tue, 24 Mar 2020 00:28:38 GMT  
		Size: 4.3 KB (4260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21f5512bc1e959ad2111ec23d41495a84d5ca7892972c6dff7269b0ce4b05ca`  
		Last Modified: Tue, 24 Mar 2020 00:28:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:9171d650f65087c00e9a258860ae3644cc79e93f3848a792cdba09788114abb6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57155928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdff9e5c94d0e2e4f6c78440bd749a07d1a9d342f8ae6a8c73c92977520a11b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:26:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Mon, 23 Mar 2020 23:26:17 GMT
ENV LANG=en_US.utf8
# Mon, 23 Mar 2020 23:26:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 23 Mar 2020 23:31:19 GMT
ENV PG_MAJOR=11
# Mon, 23 Mar 2020 23:31:20 GMT
ENV PG_VERSION=11.7
# Mon, 23 Mar 2020 23:31:22 GMT
ENV PG_SHA256=324ae93a8846fbb6a25d562d271bc441ffa8794654c5b2839384834de220a313
# Mon, 23 Mar 2020 23:35:34 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm9-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Mon, 23 Mar 2020 23:35:37 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Mon, 23 Mar 2020 23:35:39 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Mon, 23 Mar 2020 23:35:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 23 Mar 2020 23:35:41 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Mon, 23 Mar 2020 23:35:42 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 23 Mar 2020 23:35:42 GMT
COPY file:33e6fc6ab9ea2b87183e496ad72f1df7f682913ffd781b1451fd178b0c7d745a in /usr/local/bin/ 
# Mon, 23 Mar 2020 23:35:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 23 Mar 2020 23:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 23:35:46 GMT
EXPOSE 5432
# Mon, 23 Mar 2020 23:35:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d97752a4ca8f8fc42bf0639a04a1c8bb9244ebdf4bf1c009b9aa4e4f5f3bcd7`  
		Last Modified: Mon, 23 Mar 2020 23:45:21 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae682c8811415ca60e2e25e0806be8a3ce9ca960ca7a0d4d0b0c86a0a274956`  
		Last Modified: Mon, 23 Mar 2020 23:44:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac475721a885817929fd63c25bb34247e100be7a63d458dcb5cd9f823cdf3612`  
		Last Modified: Mon, 23 Mar 2020 23:46:05 GMT  
		Size: 54.5 MB (54523607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df36c1ea4dd3546cb6135afe0a191104c06ff9cae896d8a696817bf77d4b412a`  
		Last Modified: Mon, 23 Mar 2020 23:45:46 GMT  
		Size: 7.6 KB (7574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87749f588e1ca17234f132a38fa6d791eed2d1bee7aa1b937d3052a611ef176`  
		Last Modified: Mon, 23 Mar 2020 23:45:46 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23faee9ef18704fb45e995f16367456a7062475871983fe02d464746b49ba9ca`  
		Last Modified: Mon, 23 Mar 2020 23:45:46 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cace94182dc68c5c592e1d7a6ceec6f3120711fab96ee736d5f1478aa24267`  
		Last Modified: Mon, 23 Mar 2020 23:45:46 GMT  
		Size: 4.3 KB (4265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0d0527c64d814bed8dd608ade7316e038c88e8fab266f28325a6a7190ff5c0`  
		Last Modified: Mon, 23 Mar 2020 23:45:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:4e86d8640ae7068ad7752b6029ee1c5e0c31d2ed2b6b4b612a832809f4ab3a55
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54464513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925cee2a81c07429ab8efb14881477afa386d3b1f79b2d68cee637452f525e4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:43:21 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Mon, 23 Mar 2020 22:43:21 GMT
ENV LANG=en_US.utf8
# Mon, 23 Mar 2020 22:43:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 23 Mar 2020 22:49:03 GMT
ENV PG_MAJOR=11
# Mon, 23 Mar 2020 22:49:07 GMT
ENV PG_VERSION=11.7
# Mon, 23 Mar 2020 22:49:08 GMT
ENV PG_SHA256=324ae93a8846fbb6a25d562d271bc441ffa8794654c5b2839384834de220a313
# Mon, 23 Mar 2020 22:52:21 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm9-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Mon, 23 Mar 2020 22:52:38 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Mon, 23 Mar 2020 22:52:43 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Mon, 23 Mar 2020 22:52:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 23 Mar 2020 22:52:45 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Mon, 23 Mar 2020 22:52:46 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 23 Mar 2020 22:52:47 GMT
COPY file:33e6fc6ab9ea2b87183e496ad72f1df7f682913ffd781b1451fd178b0c7d745a in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:52:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 23 Mar 2020 22:52:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:52:51 GMT
EXPOSE 5432
# Mon, 23 Mar 2020 22:52:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48d9b30ccc2f0daa550064546b02eddaa410c0a5ff36be31fc55c747b40e0ad`  
		Last Modified: Mon, 23 Mar 2020 23:02:11 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59176775d1234d40a9b589b93b12933263fc13cde3b8672653317d01d4203e6`  
		Last Modified: Mon, 23 Mar 2020 23:02:11 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2150c6ba3e85d1502012a9b4a1f6a34b69afc8eefe6c2d341a46b79d21341bde`  
		Last Modified: Mon, 23 Mar 2020 23:02:47 GMT  
		Size: 52.0 MB (52030287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad00e5a503fb573733244a190c5e7c4e3a9e344b5b584556a4673d632511d3a3`  
		Last Modified: Mon, 23 Mar 2020 23:02:30 GMT  
		Size: 7.6 KB (7571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8c171816ed2ea6dda9e43817c60910ef1cae9b7c2c9801f808ebdf0fb96e36`  
		Last Modified: Mon, 23 Mar 2020 23:02:30 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e9a3f2ce480a560716e2c70cdc414c1870d1afb85a6721ebaf14ba4cc5359e`  
		Last Modified: Mon, 23 Mar 2020 23:02:30 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba84b6aef2ab86f70dc94f3e465d8d70c87744ef33023da38710923f1bd9bd25`  
		Last Modified: Mon, 23 Mar 2020 23:02:30 GMT  
		Size: 4.3 KB (4263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae8e1689036c43c5f004d3b2f9a203a90d6bca322bfbd43545f23e6fdd5919b`  
		Last Modified: Mon, 23 Mar 2020 23:02:30 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:a0112eaeaef8e476b1b092711ad1e7957f0b5bb67507e41807c4abf913c49d96
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58392089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf095ad1449a2393e4219d8b4827b94bdc717d4ad38b6b63ce48757e94ab6449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:26:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Mon, 23 Mar 2020 23:26:17 GMT
ENV LANG=en_US.utf8
# Mon, 23 Mar 2020 23:26:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 23 Mar 2020 23:30:06 GMT
ENV PG_MAJOR=11
# Mon, 23 Mar 2020 23:30:07 GMT
ENV PG_VERSION=11.7
# Mon, 23 Mar 2020 23:30:07 GMT
ENV PG_SHA256=324ae93a8846fbb6a25d562d271bc441ffa8794654c5b2839384834de220a313
# Mon, 23 Mar 2020 23:33:40 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm9-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Mon, 23 Mar 2020 23:33:43 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Mon, 23 Mar 2020 23:33:45 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Mon, 23 Mar 2020 23:33:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 23 Mar 2020 23:33:47 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Mon, 23 Mar 2020 23:33:48 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 23 Mar 2020 23:33:48 GMT
COPY file:33e6fc6ab9ea2b87183e496ad72f1df7f682913ffd781b1451fd178b0c7d745a in /usr/local/bin/ 
# Mon, 23 Mar 2020 23:33:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 23 Mar 2020 23:33:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 23:33:51 GMT
EXPOSE 5432
# Mon, 23 Mar 2020 23:33:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf70ccdbfa7098e9140b79b24406b2b9d982a82a0a28d57d23a96773cb603b5`  
		Last Modified: Mon, 23 Mar 2020 23:44:02 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae682c8811415ca60e2e25e0806be8a3ce9ca960ca7a0d4d0b0c86a0a274956`  
		Last Modified: Mon, 23 Mar 2020 23:44:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea21322fc886872fca215d660ea6d683f600bf36f339417059e6fd06c4a0819c`  
		Last Modified: Mon, 23 Mar 2020 23:44:37 GMT  
		Size: 55.7 MB (55655214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecb8c4f56a93ad29361dd63165ad5df60e986e5ba3113a7496d09b82725613a`  
		Last Modified: Mon, 23 Mar 2020 23:44:21 GMT  
		Size: 7.6 KB (7570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e1f0c520b1ec539e7d268ece445733976ed0c8cb9961d53a1752d892bb8471`  
		Last Modified: Mon, 23 Mar 2020 23:44:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e5fb53dfdaf5a117a7003d8a53c3590d599bf963e67a77ea13db247c60a91e`  
		Last Modified: Mon, 23 Mar 2020 23:44:21 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb39175fdd2a6ee217323cf26255b528b530bb32b1c376dd05ec34c602f8aaff`  
		Last Modified: Mon, 23 Mar 2020 23:44:21 GMT  
		Size: 4.3 KB (4259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525a9824801b902588f78bcf0dd9d76e382b640fc8c79f9cb6d93f8d3b4b16e6`  
		Last Modified: Mon, 23 Mar 2020 23:44:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; 386

```console
$ docker pull postgres@sha256:1e352ecbf82fc8eb50c6920b77484a35e22defed1d2118adc40d4fd1a8a32774
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62004868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5897e2238a20191b4b031131e65d6e88f7d4f21c6592cbd85c889bfb4e2e271`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Mar 2020 21:38:28 GMT
ADD file:99c8234abafd4fa915c0b826eb0e3be0e6aaa7c1e33cb1214ef71a99e9c02e06 in / 
# Mon, 23 Mar 2020 21:38:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 02:01:01 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 24 Mar 2020 02:01:01 GMT
ENV LANG=en_US.utf8
# Tue, 24 Mar 2020 02:01:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 24 Mar 2020 02:12:24 GMT
ENV PG_MAJOR=11
# Tue, 24 Mar 2020 02:12:24 GMT
ENV PG_VERSION=11.7
# Tue, 24 Mar 2020 02:12:24 GMT
ENV PG_SHA256=324ae93a8846fbb6a25d562d271bc441ffa8794654c5b2839384834de220a313
# Tue, 24 Mar 2020 02:22:36 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm9-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Tue, 24 Mar 2020 02:22:37 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 24 Mar 2020 02:22:38 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 24 Mar 2020 02:22:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 24 Mar 2020 02:22:39 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 24 Mar 2020 02:22:39 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 24 Mar 2020 02:22:39 GMT
COPY file:33e6fc6ab9ea2b87183e496ad72f1df7f682913ffd781b1451fd178b0c7d745a in /usr/local/bin/ 
# Tue, 24 Mar 2020 02:22:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 24 Mar 2020 02:22:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2020 02:22:40 GMT
EXPOSE 5432
# Tue, 24 Mar 2020 02:22:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:43f6a4398e1c9e860dfb5c93d7049ab9eedf814513bd6d07e06077c560303c7a`  
		Last Modified: Mon, 23 Mar 2020 21:38:48 GMT  
		Size: 2.8 MB (2806122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cdf55f7a0aa0a693844419981d81c70054f4bc176f69e991a997bef43eb26b0`  
		Last Modified: Tue, 24 Mar 2020 02:41:28 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da5023fc51830a3c2363157395875af5c493b6c0bd05ce36d1b47771b691560`  
		Last Modified: Tue, 24 Mar 2020 02:41:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cda6db51a70d3b02a893c025401b8b657cd17e085c01959ba30a1fb03ee42f`  
		Last Modified: Tue, 24 Mar 2020 02:42:23 GMT  
		Size: 59.2 MB (59185142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4469b405610974cb0dd65500121c373536bd6bb4cfb43aff3ed58e18313817af`  
		Last Modified: Tue, 24 Mar 2020 02:41:49 GMT  
		Size: 7.6 KB (7572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6db3cf324d4969f3c8bd56c3fbff442f4ef2daba6483bf319db4e96546123d`  
		Last Modified: Tue, 24 Mar 2020 02:41:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f782bb8b254faf70368c76725cd6ded0189e18d1febccc772d41714119a176`  
		Last Modified: Tue, 24 Mar 2020 02:41:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a1850c49d084fb29599eac2af1bd562585f1a6d49d1048994036f96b103d51`  
		Last Modified: Tue, 24 Mar 2020 02:41:50 GMT  
		Size: 4.3 KB (4257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0e7cfa3e543be804ca47d4dc03deda5d3b4566588d3c53eb032e6765d0a087`  
		Last Modified: Tue, 24 Mar 2020 02:41:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:402ab96d809b88e3278e7b16044b47138a80b23b830c0bec7adabd1511055185
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61012956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c170373f0c2250a349f46a56e03b630aa91cb3ac5b2b1451ea40f2d56a8a4cdf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Mar 2020 21:21:29 GMT
ADD file:4b35131542b9682214e1c2c72fe3cea215a10e2f775e87befecd80fe2228d5a0 in / 
# Mon, 23 Mar 2020 21:21:32 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:32:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Mon, 23 Mar 2020 23:32:58 GMT
ENV LANG=en_US.utf8
# Mon, 23 Mar 2020 23:33:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 23 Mar 2020 23:39:51 GMT
ENV PG_MAJOR=11
# Mon, 23 Mar 2020 23:39:55 GMT
ENV PG_VERSION=11.7
# Mon, 23 Mar 2020 23:39:57 GMT
ENV PG_SHA256=324ae93a8846fbb6a25d562d271bc441ffa8794654c5b2839384834de220a313
# Mon, 23 Mar 2020 23:45:53 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm9-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Mon, 23 Mar 2020 23:46:03 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Mon, 23 Mar 2020 23:46:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Mon, 23 Mar 2020 23:46:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 23 Mar 2020 23:46:24 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Mon, 23 Mar 2020 23:46:27 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 23 Mar 2020 23:46:29 GMT
COPY file:33e6fc6ab9ea2b87183e496ad72f1df7f682913ffd781b1451fd178b0c7d745a in /usr/local/bin/ 
# Mon, 23 Mar 2020 23:46:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 23 Mar 2020 23:46:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:45 GMT
EXPOSE 5432
# Mon, 23 Mar 2020 23:46:49 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bc1c99f4ba60de0d3ca52dc6855483e24c91884e33df71f502bbff6eb909d9b9`  
		Last Modified: Mon, 23 Mar 2020 21:22:12 GMT  
		Size: 2.8 MB (2820052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e24e77bb4bdf10a12615b518d92fce4871d89df08c615afd1a51053ecd5c06`  
		Last Modified: Mon, 23 Mar 2020 23:59:59 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b08df00f3eac9768a1a5e068c9cb9a8c20ffd792fb8c287b085bf72dd4cf362`  
		Last Modified: Mon, 23 Mar 2020 23:59:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a572c49f3cecd0f55eae3e3b4f8b75cc2b3d92cd995a764018bb00dfc1635040`  
		Last Modified: Tue, 24 Mar 2020 00:00:40 GMT  
		Size: 58.2 MB (58179165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881b0d3486fc5fe6c88e4dffbe02ae185ca544675f083aea5c65a3a988aa5c92`  
		Last Modified: Tue, 24 Mar 2020 00:00:25 GMT  
		Size: 7.6 KB (7573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09538e3ac2219e52f68bedc102aabed66ebdfae991bb7737ac3d8e88ad53ee70`  
		Last Modified: Tue, 24 Mar 2020 00:00:25 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c78db46f193fdd38de460ce0319f5db7278074aac3a5c7bcdf053caf9e06fbd`  
		Last Modified: Tue, 24 Mar 2020 00:00:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822a84e8ce0731c8b68fa35ad95b85cda06867794dde581bdf5091d692e95f8e`  
		Last Modified: Tue, 24 Mar 2020 00:00:25 GMT  
		Size: 4.3 KB (4263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3026db6eb99bd08e13af413b53bdeda74fd1a0964eb98fe8529c36d898863423`  
		Last Modified: Tue, 24 Mar 2020 00:00:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:e49264a2aafa2d71607bf05d06fbc2a4bc2f5372208bb4bd06cf08293d0462f4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60762685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8db85abb7974e0df7e600c6d6b58f9feb4e12e26747bb0f60aff6c29c15ebfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Mar 2020 21:41:34 GMT
ADD file:b6d4ad8fd0ec7f66e6d54b8cd8937ba7821b44096806af78692b4cab6d087a9c in / 
# Mon, 23 Mar 2020 21:41:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:34:53 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Mon, 23 Mar 2020 22:34:54 GMT
ENV LANG=en_US.utf8
# Mon, 23 Mar 2020 22:34:56 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 23 Mar 2020 22:40:32 GMT
ENV PG_MAJOR=11
# Mon, 23 Mar 2020 22:40:32 GMT
ENV PG_VERSION=11.7
# Mon, 23 Mar 2020 22:40:33 GMT
ENV PG_SHA256=324ae93a8846fbb6a25d562d271bc441ffa8794654c5b2839384834de220a313
# Mon, 23 Mar 2020 22:46:22 GMT
RUN set -ex 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		openssl 		tar 		&& wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2" 	&& echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c - 	&& mkdir -p /usr/src/postgresql 	&& tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	&& rm postgresql.tar.bz2 		&& apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm9-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 		&& cd /usr/src/postgresql 	&& awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new 	&& grep '/var/run/postgresql' src/include/pg_config_manual.h.new 	&& mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb' 	&& ./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	&& make -j "$(nproc)" world 	&& make install-world 	&& make -C contrib install 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	&& apk del .fetch-deps .build-deps 	&& cd / 	&& rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	&& find /usr/local -name '*.a' -delete
# Mon, 23 Mar 2020 22:46:31 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Mon, 23 Mar 2020 22:46:32 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Mon, 23 Mar 2020 22:46:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 23 Mar 2020 22:46:34 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Mon, 23 Mar 2020 22:46:35 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 23 Mar 2020 22:46:35 GMT
COPY file:33e6fc6ab9ea2b87183e496ad72f1df7f682913ffd781b1451fd178b0c7d745a in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:46:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 23 Mar 2020 22:46:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:46:38 GMT
EXPOSE 5432
# Mon, 23 Mar 2020 22:46:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ca1c6795bfb97df28a926fd646127ba4944b69beb1cea7b00d62787b8b3c0108`  
		Last Modified: Mon, 23 Mar 2020 21:41:56 GMT  
		Size: 2.6 MB (2582073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096988d6f0d7fbd4d835bbdd287617d11694ddc413c08e121fb9e04ac568179e`  
		Last Modified: Mon, 23 Mar 2020 22:56:13 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac69069693ec79fe32bc3463632dd40d67b35b256844d6a7bd05a596226684d`  
		Last Modified: Mon, 23 Mar 2020 22:56:11 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48604f2afa55e9fb129d1b4d5140ecadd263866de331277da02447c9b4d29265`  
		Last Modified: Mon, 23 Mar 2020 22:56:41 GMT  
		Size: 58.2 MB (58166878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588c118014dda6c4aa4d1aae3a2a5b95caf0d5001b13ee9e067d9a940f248d66`  
		Last Modified: Mon, 23 Mar 2020 22:56:31 GMT  
		Size: 7.6 KB (7571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5e99591f9ba7ad0436a290329cd3df1ef5612ad8c9c127cdcb4709e0603180`  
		Last Modified: Mon, 23 Mar 2020 22:56:31 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5079db2b8c1645d50062214db452a7c78df7d81b40c55ec1002f6ba99c2fd2c`  
		Last Modified: Mon, 23 Mar 2020 22:56:31 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b97238532f6f12d7641e7187ab874d48857932c6927a72c695a8a1a0c57ada`  
		Last Modified: Mon, 23 Mar 2020 22:56:46 GMT  
		Size: 4.3 KB (4262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd5e2c7707676652cc55890afbea0ab3ad2473ae1043e2edc71a814d2790118`  
		Last Modified: Mon, 23 Mar 2020 22:56:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
