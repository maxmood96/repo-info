## `postgres:13-alpine`

```console
$ docker pull postgres@sha256:d7f4c46ada617bca23a582b2f42499ca27767f33e0b8f7607553dcff5d493640
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

### `postgres:13-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:e06c50d5582ec9571164b97533864af27365f177036c917ca2b056d5d39f449b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62270511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc401b315beb703e996ab0ef1f8601388299289b59aa53c81c4a3fdb0bc30a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 15:26:36 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 12 Mar 2021 15:26:36 GMT
ENV LANG=en_US.utf8
# Fri, 12 Mar 2021 15:26:37 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Mar 2021 15:26:37 GMT
ENV PG_MAJOR=13
# Fri, 12 Mar 2021 15:26:37 GMT
ENV PG_VERSION=13.2
# Fri, 12 Mar 2021 15:26:37 GMT
ENV PG_SHA256=5fd7fcd08db86f5b2aed28fcfaf9ae0aca8e9428561ac547764c2a2b0f41adfc
# Fri, 12 Mar 2021 15:32:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 12 Mar 2021 15:32:25 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 12 Mar 2021 15:32:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 12 Mar 2021 15:32:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 12 Mar 2021 15:32:28 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 12 Mar 2021 15:32:28 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 12 Mar 2021 15:32:28 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Fri, 12 Mar 2021 15:32:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Mar 2021 15:32:29 GMT
STOPSIGNAL SIGINT
# Fri, 12 Mar 2021 15:32:29 GMT
EXPOSE 5432
# Fri, 12 Mar 2021 15:32:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba41e371f09ceda8ea570b685d8f7db61c8615eadf30756d81a62f7d61289a74`  
		Last Modified: Fri, 12 Mar 2021 16:06:01 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ca07debf1d3613aa92cbe55cf0578603c9c9ae5c089c320f890ce41820f58a`  
		Last Modified: Fri, 12 Mar 2021 16:06:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2bd1da05b177592358abb6fc703a3bf56939b2bdb20ee85ba00ec2ab83af83`  
		Last Modified: Fri, 12 Mar 2021 16:06:07 GMT  
		Size: 59.4 MB (59444104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5213e78ba6e27990cf8a4f91f0462140a15342ce6bb47827d5523d0fda539590`  
		Last Modified: Fri, 12 Mar 2021 16:05:54 GMT  
		Size: 8.6 KB (8561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1c1247fd1f7ea4e873f27b746b5d5b0fe5a29d97277c3114b0bbcfed077476`  
		Last Modified: Fri, 12 Mar 2021 16:05:54 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c298f42ee8c52d66b31b17a8ab01bf586676aed0e0c5ceb877e17324dbbdfdc`  
		Last Modified: Fri, 12 Mar 2021 16:05:54 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a176aff6d18fc5349231f52c77f67d43167d0753367ab7f4011a104d370d220`  
		Last Modified: Fri, 12 Mar 2021 16:05:54 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:15710d66eb3d5eb252c9809c3828e75686422c9f5b66d96b947effe53b995cb3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60575695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5da678dc335b77157f0293859a6789358b2c7c1b6f020e9c4c261c3b62807a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 23:03:42 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 17 Feb 2021 23:03:42 GMT
ENV LANG=en_US.utf8
# Wed, 17 Feb 2021 23:03:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Feb 2021 23:03:46 GMT
ENV PG_MAJOR=13
# Wed, 17 Feb 2021 23:03:47 GMT
ENV PG_VERSION=13.2
# Wed, 17 Feb 2021 23:03:48 GMT
ENV PG_SHA256=5fd7fcd08db86f5b2aed28fcfaf9ae0aca8e9428561ac547764c2a2b0f41adfc
# Wed, 17 Feb 2021 23:07:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 17 Feb 2021 23:07:47 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 17 Feb 2021 23:07:49 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 17 Feb 2021 23:07:50 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 17 Feb 2021 23:07:52 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 17 Feb 2021 23:07:53 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 17 Feb 2021 23:07:53 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Wed, 17 Feb 2021 23:07:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 23:07:55 GMT
STOPSIGNAL SIGINT
# Wed, 17 Feb 2021 23:07:56 GMT
EXPOSE 5432
# Wed, 17 Feb 2021 23:07:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c466870a71b73094e5a73a7e0fdf9e0fc7a2def8525ea7665bc5b3e382f8b4`  
		Last Modified: Wed, 17 Feb 2021 23:27:05 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754cb30576f658b66484126890351d63b0bbecd0aff43d7ff597325359d00112`  
		Last Modified: Wed, 17 Feb 2021 23:27:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a218b3ccbba5eaaa1ce2a4a84fccb6d849af46ec9392f7ec5597b439c7596ac7`  
		Last Modified: Wed, 17 Feb 2021 23:27:19 GMT  
		Size: 57.9 MB (57938906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e01a1f4842fe4c2306da43ecb3b550acc4b867379460e327497e986bde473c4`  
		Last Modified: Wed, 17 Feb 2021 23:27:01 GMT  
		Size: 8.6 KB (8562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efcf78778074e499c580573f8c9e4c8a71789d96473958876e15e48180255335`  
		Last Modified: Wed, 17 Feb 2021 23:27:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3b34f3e0e859ad9818fb13ea5678c229edf18a97b7e424c98d3f998e9d6539`  
		Last Modified: Wed, 17 Feb 2021 23:27:01 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e3451552e405d085bb04b92f7bac4bf125f364b8670d267219137e30c5d227`  
		Last Modified: Wed, 17 Feb 2021 23:27:01 GMT  
		Size: 4.4 KB (4407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:de176f849feaf80556f303dca983d75e9b160a619d14b00186228e0f7e83f46c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57608309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6861317df4e3fb051d890a58dd9244ac84157f48f6f7507ef5f698e079bfab11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 23:38:05 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 17 Feb 2021 23:38:06 GMT
ENV LANG=en_US.utf8
# Wed, 17 Feb 2021 23:38:08 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Feb 2021 23:38:09 GMT
ENV PG_MAJOR=13
# Wed, 17 Feb 2021 23:38:09 GMT
ENV PG_VERSION=13.2
# Wed, 17 Feb 2021 23:38:10 GMT
ENV PG_SHA256=5fd7fcd08db86f5b2aed28fcfaf9ae0aca8e9428561ac547764c2a2b0f41adfc
# Wed, 17 Feb 2021 23:41:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 17 Feb 2021 23:41:42 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 17 Feb 2021 23:41:44 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 17 Feb 2021 23:41:45 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 17 Feb 2021 23:41:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 17 Feb 2021 23:41:47 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 17 Feb 2021 23:41:48 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Wed, 17 Feb 2021 23:41:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 23:41:50 GMT
STOPSIGNAL SIGINT
# Wed, 17 Feb 2021 23:41:51 GMT
EXPOSE 5432
# Wed, 17 Feb 2021 23:41:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a02e78d0690510cbbcaf122beefdfd0be6106291820f5db4dcc3b6d0e28dfc8`  
		Last Modified: Thu, 18 Feb 2021 00:00:39 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671c6d1d98c310b550014b6a6f6f5e38df97f28413e21c08391b2771130a5c74`  
		Last Modified: Thu, 18 Feb 2021 00:00:39 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ca676cf4c7b9a685598761613fe1b43381eab8def56b8b6a4897990ef1dece`  
		Last Modified: Thu, 18 Feb 2021 00:00:53 GMT  
		Size: 55.2 MB (55169668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329df546071b88ff77a1dc22d449b9a153540bb39af0820edb2e477ebab33f0e`  
		Last Modified: Thu, 18 Feb 2021 00:00:38 GMT  
		Size: 8.6 KB (8562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4baaf670337b9e7cd36dc944186d77a5a80e78d88bdc2fa8086c636c6403234`  
		Last Modified: Thu, 18 Feb 2021 00:00:38 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f2fd97d19f16d3f33b22e2adb4b8adb54a66c2c5948ee277be6464992231fe`  
		Last Modified: Thu, 18 Feb 2021 00:00:38 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf939b314ef081356d8dfedaa0629963702e24f56c7932e9ade00e018d8bc25`  
		Last Modified: Thu, 18 Feb 2021 00:00:38 GMT  
		Size: 4.4 KB (4407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:2cc83c58ec17eb6461d76f27db77af8b745d767a6b7bbbfd79f6754d203afe3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61543127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3edd80e86e2d755a6435f0d58ec8fe5da05415d662f95f5af1e3efc0a4b2d78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 23:15:04 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 17 Feb 2021 23:15:05 GMT
ENV LANG=en_US.utf8
# Wed, 17 Feb 2021 23:15:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Feb 2021 23:15:08 GMT
ENV PG_MAJOR=13
# Wed, 17 Feb 2021 23:15:08 GMT
ENV PG_VERSION=13.2
# Wed, 17 Feb 2021 23:15:09 GMT
ENV PG_SHA256=5fd7fcd08db86f5b2aed28fcfaf9ae0aca8e9428561ac547764c2a2b0f41adfc
# Wed, 17 Feb 2021 23:19:00 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 17 Feb 2021 23:19:03 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 17 Feb 2021 23:19:05 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 17 Feb 2021 23:19:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 17 Feb 2021 23:19:08 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 17 Feb 2021 23:19:09 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 17 Feb 2021 23:19:09 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Wed, 17 Feb 2021 23:19:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 23:19:11 GMT
STOPSIGNAL SIGINT
# Wed, 17 Feb 2021 23:19:12 GMT
EXPOSE 5432
# Wed, 17 Feb 2021 23:19:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea767c0e0b823455a91d082e4db47af65e6aa51a78df49f9700eb9e21245f8d`  
		Last Modified: Wed, 17 Feb 2021 23:38:53 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65dac6dbfdc3c658a4293d3279f8b00d5ba7fb3b2793c0e984f39a0a25d8b34`  
		Last Modified: Wed, 17 Feb 2021 23:38:53 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0408b22bcf027068c3a8b7f3ae8773db531ba34f7e83b56741552cdfd9d49d95`  
		Last Modified: Wed, 17 Feb 2021 23:39:08 GMT  
		Size: 58.8 MB (58816808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72309a967e236197e87c8fd8006545bef87752403784fa22c54234fb734b97a0`  
		Last Modified: Wed, 17 Feb 2021 23:38:52 GMT  
		Size: 8.6 KB (8561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe79acafade77b19128a6587afa233f38f57da41497aaeb64ac9f22dc7b840b`  
		Last Modified: Wed, 17 Feb 2021 23:38:51 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83fe4d2595b7633aa6266005289f04957707051e9abe20a61d2183822140a9ae`  
		Last Modified: Wed, 17 Feb 2021 23:38:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3764f6f685b422d614cacaf389b1412d9c6e0c45d4fce87e2217223b6137da6`  
		Last Modified: Wed, 17 Feb 2021 23:38:51 GMT  
		Size: 4.4 KB (4405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine` - linux; 386

```console
$ docker pull postgres@sha256:ace6ae9bf4c2961da6a5e227a57e34e8b39d3b3652b5725e61f8e6f5d984ada4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65851253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7eac138f6bb88827395bd0decfaa2bcab7f7819440560de487197441e37b8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 20:22:42 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 12 Mar 2021 20:22:43 GMT
ENV LANG=en_US.utf8
# Fri, 12 Mar 2021 20:22:43 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Mar 2021 20:22:44 GMT
ENV PG_MAJOR=13
# Fri, 12 Mar 2021 20:22:44 GMT
ENV PG_VERSION=13.2
# Fri, 12 Mar 2021 20:22:44 GMT
ENV PG_SHA256=5fd7fcd08db86f5b2aed28fcfaf9ae0aca8e9428561ac547764c2a2b0f41adfc
# Fri, 12 Mar 2021 20:30:27 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 12 Mar 2021 20:30:29 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 12 Mar 2021 20:30:30 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 12 Mar 2021 20:30:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 12 Mar 2021 20:30:31 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 12 Mar 2021 20:30:31 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 12 Mar 2021 20:30:31 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Fri, 12 Mar 2021 20:30:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Mar 2021 20:30:32 GMT
STOPSIGNAL SIGINT
# Fri, 12 Mar 2021 20:30:32 GMT
EXPOSE 5432
# Fri, 12 Mar 2021 20:30:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e729ac31be078df1147e7d573e4eae1419b7e8af9e15f0a1d1c82ca4e57e8b0f`  
		Last Modified: Fri, 12 Mar 2021 21:06:54 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8d26371d9431aa45553c82bf8bd7314116c124e7aa94a92da6992533c2ec16`  
		Last Modified: Fri, 12 Mar 2021 21:06:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29c1eb7883fbf6ed7343420ef372eeaa8b822847dc61675ed4a83064c514486`  
		Last Modified: Fri, 12 Mar 2021 21:07:12 GMT  
		Size: 63.0 MB (63018328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d905d85cb3224585114703c976708c001420159fc34b706fdd1db2e31d5231`  
		Last Modified: Fri, 12 Mar 2021 21:06:52 GMT  
		Size: 8.6 KB (8565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120f116311623ef3aa14d89c8b460accf1c6f293a3ef5abb6bfea54f49ed02a1`  
		Last Modified: Fri, 12 Mar 2021 21:06:52 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b120a0bb13fedc7914225be3831dfafec7ee4aa568e028c444c16e7112450048`  
		Last Modified: Fri, 12 Mar 2021 21:06:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548d736c215978087115315be5c4977aeb8f583a8f138843c23ddf2eb227dddb`  
		Last Modified: Fri, 12 Mar 2021 21:06:52 GMT  
		Size: 4.4 KB (4402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:d5c0a35ef04a9dd9a15e1af0db137ba78153b35729123ebf83fe70967b5368f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64694031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7674e6ce02f8461c6942369d82a8fc40b05633ca9dae9a6ec234abe83b41bbf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 23:40:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 17 Feb 2021 23:40:45 GMT
ENV LANG=en_US.utf8
# Wed, 17 Feb 2021 23:40:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Feb 2021 23:40:57 GMT
ENV PG_MAJOR=13
# Wed, 17 Feb 2021 23:41:00 GMT
ENV PG_VERSION=13.2
# Wed, 17 Feb 2021 23:41:11 GMT
ENV PG_SHA256=5fd7fcd08db86f5b2aed28fcfaf9ae0aca8e9428561ac547764c2a2b0f41adfc
# Wed, 17 Feb 2021 23:45:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 17 Feb 2021 23:45:38 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 17 Feb 2021 23:45:45 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 17 Feb 2021 23:45:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 17 Feb 2021 23:46:04 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 17 Feb 2021 23:46:06 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 17 Feb 2021 23:46:08 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Wed, 17 Feb 2021 23:46:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 23:46:16 GMT
STOPSIGNAL SIGINT
# Wed, 17 Feb 2021 23:46:22 GMT
EXPOSE 5432
# Wed, 17 Feb 2021 23:46:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62347ea12b2b66d9d40b3e5b53079b8dab0d76d44bc63abf4361dde7a9d2fd6`  
		Last Modified: Thu, 18 Feb 2021 00:16:49 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e195dedf606bdd9ff225564397fb91e0bfd068b1e74cb7c243e7a9026192471`  
		Last Modified: Thu, 18 Feb 2021 00:16:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c5a295f69525696009c2624929d0f19ecf1f5d41372d3994564349c35fb74a`  
		Last Modified: Thu, 18 Feb 2021 00:16:59 GMT  
		Size: 61.9 MB (61866202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e25deca9c1f583aa268597d23e3a508934a6b033b274ff9bfe3101c0152e9b4`  
		Last Modified: Thu, 18 Feb 2021 00:16:46 GMT  
		Size: 8.6 KB (8561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a40f99f810d5dfb8a8df5d8c247a08a5d452bf100b3def36653440425f068`  
		Last Modified: Thu, 18 Feb 2021 00:16:46 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae58dc2d984d6ad6fb19f11280fefdd3eb91c8bbcc326f8ee10eb937349aff`  
		Last Modified: Thu, 18 Feb 2021 00:16:46 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8ca743104e5b18efff76ed9386d6897563cba19447e1a8164935bfcb613bdc`  
		Last Modified: Thu, 18 Feb 2021 00:16:46 GMT  
		Size: 4.4 KB (4404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:200d6d0f8f8aa6366dd1b78742d218c00ec8a5343faa71ec4f874681af79a825
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (65020970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1ce790fb7499856701bfa7c379cebfde64d5f00f7d231ea1867cf592a17197`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:54:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 18 Feb 2021 01:54:30 GMT
ENV LANG=en_US.utf8
# Thu, 18 Feb 2021 01:54:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 18 Feb 2021 01:54:31 GMT
ENV PG_MAJOR=13
# Thu, 18 Feb 2021 01:54:31 GMT
ENV PG_VERSION=13.2
# Thu, 18 Feb 2021 01:54:31 GMT
ENV PG_SHA256=5fd7fcd08db86f5b2aed28fcfaf9ae0aca8e9428561ac547764c2a2b0f41adfc
# Thu, 18 Feb 2021 01:57:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 18 Feb 2021 01:57:40 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 18 Feb 2021 01:57:41 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 18 Feb 2021 01:57:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Feb 2021 01:57:42 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 18 Feb 2021 01:57:42 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Feb 2021 01:57:42 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 18 Feb 2021 01:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 01:57:43 GMT
STOPSIGNAL SIGINT
# Thu, 18 Feb 2021 01:57:43 GMT
EXPOSE 5432
# Thu, 18 Feb 2021 01:57:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da53daa845ee16c5cb762996a474aa4ecac04e53b3578031254225e63f573164`  
		Last Modified: Thu, 18 Feb 2021 02:11:15 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05dfcde47a8d8d175de0042dd1d418474b9ff7acfa08d97a3d46ba82ea562c8e`  
		Last Modified: Thu, 18 Feb 2021 02:11:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328181c0da36c133b33df82f76eb8f7485d72372738a0ad5fd3f7f2f6ad1afe6`  
		Last Modified: Thu, 18 Feb 2021 02:11:21 GMT  
		Size: 62.4 MB (62403845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2511a9dd6c404600fb8cf62e11be27c627a54459532ae2393eff2e8ba7e03bf6`  
		Last Modified: Thu, 18 Feb 2021 02:11:14 GMT  
		Size: 8.6 KB (8559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e6b670b9e18f12da908385f76c95eeebc7fe77297de550624586389abd23ef`  
		Last Modified: Thu, 18 Feb 2021 02:11:13 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238fd0df8099c1d5d9dcba4dfd41636e42d48ca69efc0749e8dab312a757745a`  
		Last Modified: Thu, 18 Feb 2021 02:11:14 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755605044f663fd115c186c4c16f991bcc9d1c2ab5f737a77243e0205ba0ac89`  
		Last Modified: Thu, 18 Feb 2021 02:11:13 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
