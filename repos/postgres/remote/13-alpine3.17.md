## `postgres:13-alpine3.17`

```console
$ docker pull postgres@sha256:937c644a6879ac26e0faab1c9b6b12f8a010268e53d141b5d3afd432cc69f0b5
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
$ docker pull postgres@sha256:10fbc4f33a56869bf1f0eaba68778a3adb14fa9376e54f067a6498610a10d31e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92070207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92afc4824d0f763607673e6307b2640f0008b995356ba70acfdbf4b2cbe77bda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 21:13:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 14 Jun 2023 21:13:15 GMT
ENV LANG=en_US.utf8
# Wed, 14 Jun 2023 21:13:16 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jun 2023 21:31:45 GMT
ENV PG_MAJOR=13
# Wed, 14 Jun 2023 21:31:46 GMT
ENV PG_VERSION=13.11
# Wed, 14 Jun 2023 21:31:46 GMT
ENV PG_SHA256=4992ff647203566b670d4e54dc5317499a26856c93576d0ea951bdf6bee50bfb
# Wed, 14 Jun 2023 21:31:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 14 Jun 2023 21:34:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 14 Jun 2023 21:34:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 14 Jun 2023 21:34:18 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Wed, 14 Jun 2023 21:34:18 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 14 Jun 2023 21:34:18 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Wed, 14 Jun 2023 21:34:18 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 14 Jun 2023 21:34:18 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Wed, 14 Jun 2023 21:34:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 21:34:19 GMT
STOPSIGNAL SIGINT
# Wed, 14 Jun 2023 21:34:19 GMT
EXPOSE 5432
# Wed, 14 Jun 2023 21:34:19 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94726e0716821ec3d5f3d5b0b39ad2bce969dc1a6c20628067ab5337b37fffac`  
		Last Modified: Wed, 14 Jun 2023 21:47:14 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9106bcc0c876721d56943de59e549b33acd1aac5767c52af9b599b0741c0b8f`  
		Last Modified: Wed, 14 Jun 2023 21:47:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959108a34838d6f9f19ecd9aea1724959c3110e9049d98b67e0f4793d66c720`  
		Last Modified: Wed, 14 Jun 2023 21:51:02 GMT  
		Size: 88.7 MB (88679888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c89e3d24fca868a7af6e77de750d94357d46dd30b3be971e3eb57151880172`  
		Last Modified: Wed, 14 Jun 2023 21:50:51 GMT  
		Size: 9.0 KB (9024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02a940bec4a5b1945bdc885bf4f13324413972c982bebd613e133ad47439840`  
		Last Modified: Wed, 14 Jun 2023 21:50:51 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff193953017eeaddac99c41918c741afff2297f058d261c72958f6e9bd7098d6`  
		Last Modified: Wed, 14 Jun 2023 21:50:51 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f2deb06c749062673d52d53004579e221f985911a1259390c42fe25a63a4b1`  
		Last Modified: Wed, 14 Jun 2023 21:50:51 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine3.17` - linux; arm variant v6

```console
$ docker pull postgres@sha256:57829a9fd82d796cc6795c6c22e0b5ff6334c2fe3363f72d9a3529baebd24680
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89836563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4185354d9a4e52ed8c075e6e7e2d7a492e163259cff0e94808886b0840afe8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:25 GMT
ADD file:07e668ef139dce7f076143a30b89ff57885c8539d8b5764ac1bd5277d9936702 in / 
# Wed, 14 Jun 2023 18:49:25 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 18:59:33 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 14 Jun 2023 18:59:33 GMT
ENV LANG=en_US.utf8
# Wed, 14 Jun 2023 18:59:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jun 2023 19:19:19 GMT
ENV PG_MAJOR=13
# Wed, 14 Jun 2023 19:19:19 GMT
ENV PG_VERSION=13.11
# Wed, 14 Jun 2023 19:19:19 GMT
ENV PG_SHA256=4992ff647203566b670d4e54dc5317499a26856c93576d0ea951bdf6bee50bfb
# Wed, 14 Jun 2023 19:19:19 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 14 Jun 2023 19:22:05 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 14 Jun 2023 19:22:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 14 Jun 2023 19:22:07 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Wed, 14 Jun 2023 19:22:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 14 Jun 2023 19:22:07 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Wed, 14 Jun 2023 19:22:07 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 14 Jun 2023 19:22:07 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Wed, 14 Jun 2023 19:22:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 19:22:08 GMT
STOPSIGNAL SIGINT
# Wed, 14 Jun 2023 19:22:08 GMT
EXPOSE 5432
# Wed, 14 Jun 2023 19:22:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:33ec62e98ceea71d24212ee03e239c2d5538dbe7c98f41c42e8b2693fedf58fb`  
		Last Modified: Wed, 14 Jun 2023 18:50:00 GMT  
		Size: 3.1 MB (3110916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2beba2c9fe770149d9dfa902bba7190bc620cfc5846ca7a732a3734c1f9b2c9b`  
		Last Modified: Wed, 14 Jun 2023 19:35:12 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8cbdb5d3c82f968922b8c8a2a5d3f429eb98dbff674446bda830bd4f8bf317`  
		Last Modified: Wed, 14 Jun 2023 19:35:12 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a6ac896431a671600172560a0d0fcc67d548b561878403347025d23ed71eba`  
		Last Modified: Wed, 14 Jun 2023 19:37:51 GMT  
		Size: 86.7 MB (86710053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302cb787ecfaa94e513f866cef36d008a2c82fc7d48a93e56a4ac32a73f05632`  
		Last Modified: Wed, 14 Jun 2023 19:37:39 GMT  
		Size: 9.0 KB (9020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456e71a8640883a9a23aa2c7b6448a1f57aa67d8ff6b69c1f6f636ac0d5063f0`  
		Last Modified: Wed, 14 Jun 2023 19:37:39 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6150b495e9104fe185bb3549867e75fc43d9b84e0c62616c5ade3feaf108e20`  
		Last Modified: Wed, 14 Jun 2023 19:37:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790f7934b5b976822a93f4526f927f30c1627bc908e431ef8c43d998001c91bc`  
		Last Modified: Wed, 14 Jun 2023 19:37:39 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine3.17` - linux; arm variant v7

```console
$ docker pull postgres@sha256:a20c4cce2ebf4421975018891814cf1eaec93161da6cd2a49fc70b33d164d2de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84542958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643eaea300869725cf8869b71b0e0441da47ceabb44fb5b486a0a7491bbe26cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 14 Jun 2023 22:36:20 GMT
ADD file:5e92075a8d9a5898d661caf9c2be8a83fb25742251b4ebdc0c3d448a6dc58e4a in / 
# Wed, 14 Jun 2023 22:36:20 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 23:27:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 14 Jun 2023 23:27:39 GMT
ENV LANG=en_US.utf8
# Wed, 14 Jun 2023 23:27:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 15 Jun 2023 00:33:56 GMT
ENV PG_MAJOR=13
# Thu, 15 Jun 2023 00:33:56 GMT
ENV PG_VERSION=13.11
# Thu, 15 Jun 2023 00:33:56 GMT
ENV PG_SHA256=4992ff647203566b670d4e54dc5317499a26856c93576d0ea951bdf6bee50bfb
# Thu, 15 Jun 2023 00:33:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 15 Jun 2023 00:36:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Jun 2023 00:36:49 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Jun 2023 00:36:49 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Thu, 15 Jun 2023 00:36:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Jun 2023 00:36:50 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Thu, 15 Jun 2023 00:36:50 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Jun 2023 00:36:50 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Thu, 15 Jun 2023 00:36:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 00:36:50 GMT
STOPSIGNAL SIGINT
# Thu, 15 Jun 2023 00:36:50 GMT
EXPOSE 5432
# Thu, 15 Jun 2023 00:36:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f929d112168394cf1fbe294a86fbe5173dd92df4daac8cb09437b17dfc5df802`  
		Last Modified: Wed, 14 Jun 2023 22:37:01 GMT  
		Size: 2.9 MB (2868554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37af63edad6af9ed8a0afb123bf0ae7c5676c614ce9e0a0cf45504288b6e9c58`  
		Last Modified: Thu, 15 Jun 2023 01:15:18 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0023cd2332e5216dabe294a91ea5beb72447a95a0bb11e5c79bb32cd56402d2c`  
		Last Modified: Thu, 15 Jun 2023 01:15:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38a95302be9cbd2121ccefc2ffba167ef7f6b22a5f5312b9bc4492d4f394552`  
		Last Modified: Thu, 15 Jun 2023 01:19:11 GMT  
		Size: 81.7 MB (81658798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f332844eccf1d1256e819d165978e3941edc98b5aabb3ef5f87a6725fa4e7e`  
		Last Modified: Thu, 15 Jun 2023 01:19:01 GMT  
		Size: 9.0 KB (9024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fcbce62f8fe2c01b4d4ab2c7738217c8c6e9090f559fb41e925a0b271a2b98`  
		Last Modified: Thu, 15 Jun 2023 01:19:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3323116b81f56eefc7c037c4816d044f8f3d1dec66d202a193bf111613e046b3`  
		Last Modified: Thu, 15 Jun 2023 01:19:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d5187f24994200f8d3b9a45005b0dec77c3c57872a07aac4d3f032974c1174`  
		Last Modified: Thu, 15 Jun 2023 01:19:01 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:fc23cf0c4a09038b1ea77fbe3c06892795445de6d08f8a28cdbca1382d12276f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89824414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc104b3a3254f1a14131f7bd3c81bcaf1d0d9b28c53115f3771276913d42eae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:04 GMT
ADD file:6f6c919dc1fe5a56c2664a26a702d77203039cdd4c91e39da57063ea5d3f3094 in / 
# Wed, 14 Jun 2023 20:49:04 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 21:04:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 14 Jun 2023 21:04:39 GMT
ENV LANG=en_US.utf8
# Wed, 14 Jun 2023 21:04:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jun 2023 21:18:58 GMT
ENV PG_MAJOR=13
# Wed, 14 Jun 2023 21:18:58 GMT
ENV PG_VERSION=13.11
# Wed, 14 Jun 2023 21:18:58 GMT
ENV PG_SHA256=4992ff647203566b670d4e54dc5317499a26856c93576d0ea951bdf6bee50bfb
# Wed, 14 Jun 2023 21:18:59 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 14 Jun 2023 21:20:52 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 14 Jun 2023 21:20:53 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 14 Jun 2023 21:20:53 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Wed, 14 Jun 2023 21:20:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 14 Jun 2023 21:20:54 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Wed, 14 Jun 2023 21:20:54 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 14 Jun 2023 21:20:54 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Wed, 14 Jun 2023 21:20:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 21:20:54 GMT
STOPSIGNAL SIGINT
# Wed, 14 Jun 2023 21:20:54 GMT
EXPOSE 5432
# Wed, 14 Jun 2023 21:20:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:edb6bdbacee93be93e930669f43e2e922c8594676aa342a70e2221361fd1914d`  
		Last Modified: Wed, 14 Jun 2023 20:49:35 GMT  
		Size: 3.3 MB (3261139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8ff0e86baa37d1a94f26876e404eca60e0bff3f235c3dd9b8f04bff2b563da`  
		Last Modified: Wed, 14 Jun 2023 21:31:35 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128b35b7bff69ad7412c8b5ceabf4017d71a155e1d6dee928ffcf25678fba177`  
		Last Modified: Wed, 14 Jun 2023 21:31:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6494c822f07b52a6e384dce3390db6a2472a2e1099564f3daa7dd152dc7bf729`  
		Last Modified: Wed, 14 Jun 2023 21:34:56 GMT  
		Size: 86.5 MB (86547682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99541ec03f774dae1b763977cede3573bc93a86e3758792d2c0161a7ad1569df`  
		Last Modified: Wed, 14 Jun 2023 21:34:48 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ba952294e64416ed39982cbe813c8759ce37a0c28f5586a37ac6f166ffbd74`  
		Last Modified: Wed, 14 Jun 2023 21:34:48 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a235ad9cfd2cda3b5ce8d6cfa3307980d985e5831e8ee9b670822ba43b4a610`  
		Last Modified: Wed, 14 Jun 2023 21:34:48 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e4afd33fc0ef837cae577caf1ce1a60d7e68e23055e01a38ae9e7fd6ff5dca`  
		Last Modified: Wed, 14 Jun 2023 21:34:48 GMT  
		Size: 4.8 KB (4787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine3.17` - linux; 386

```console
$ docker pull postgres@sha256:da13917ef9fd197af67eb7887165dc322d88b717a599698bf4bda19eb988e89c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96835282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb2db9f8e09c5f5782b53f6ea4f800f247c4fed449bbc0c5e04b6d0389eba82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 14 Jun 2023 22:33:26 GMT
ADD file:39180f040ebe17a01f8b9502d7b463edade8158d87fa99e47ac0b1f369e11a65 in / 
# Wed, 14 Jun 2023 22:33:26 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 23:11:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 14 Jun 2023 23:11:47 GMT
ENV LANG=en_US.utf8
# Wed, 14 Jun 2023 23:11:48 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 15 Jun 2023 00:28:34 GMT
ENV PG_MAJOR=13
# Thu, 15 Jun 2023 00:28:34 GMT
ENV PG_VERSION=13.11
# Thu, 15 Jun 2023 00:28:34 GMT
ENV PG_SHA256=4992ff647203566b670d4e54dc5317499a26856c93576d0ea951bdf6bee50bfb
# Thu, 15 Jun 2023 00:28:34 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 15 Jun 2023 00:33:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Jun 2023 00:33:11 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Jun 2023 00:33:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Thu, 15 Jun 2023 00:33:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Jun 2023 00:33:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Thu, 15 Jun 2023 00:33:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Jun 2023 00:33:12 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Thu, 15 Jun 2023 00:33:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 00:33:12 GMT
STOPSIGNAL SIGINT
# Thu, 15 Jun 2023 00:33:12 GMT
EXPOSE 5432
# Thu, 15 Jun 2023 00:33:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:187bd96dd637d3adfc7a9b61a1e7465181bbfe90dbf7a2830dfba97e4e3243a4`  
		Last Modified: Wed, 14 Jun 2023 22:34:01 GMT  
		Size: 3.4 MB (3412675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541dbe1bafbd3cd1458e46676917913e49bd4aa2dbc3d3f8053bdde58032dd73`  
		Last Modified: Thu, 15 Jun 2023 01:21:14 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14501621fcc5e436ff61b0e4dce1b9c3709d5d9767bf8985f59c388068a5229`  
		Last Modified: Thu, 15 Jun 2023 01:21:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b18166821c8c7797c3a384d5e8ac75ff92954adbaa24b9c49729d7e92fefeb0`  
		Last Modified: Thu, 15 Jun 2023 01:26:27 GMT  
		Size: 93.4 MB (93407001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9097c2ae9668799c8e1cbc1ed5579272876a7065e5ba50903a80aa1de7854bd1`  
		Last Modified: Thu, 15 Jun 2023 01:26:10 GMT  
		Size: 9.0 KB (9024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f95e9e61b1959d5072cfca769f66e2f49f023db6b3ec358e8ae12d54873cfd9`  
		Last Modified: Thu, 15 Jun 2023 01:26:10 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1096051beca4c8705b0cb6b1c38cf9a89ac3a8909136c6ca1463d3190664ec`  
		Last Modified: Thu, 15 Jun 2023 01:26:10 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325431d79d73c74aec6d570490bc770dc198e1878dfeb5ab310a39579c9f79ba`  
		Last Modified: Thu, 15 Jun 2023 01:26:10 GMT  
		Size: 4.8 KB (4792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine3.17` - linux; ppc64le

```console
$ docker pull postgres@sha256:bb11a1a94976d10b2b48958d280aaa9aecf86e29346cca7c8a9b32f751066c5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97754452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c869568119caa95c028c30d7a8cdef5ba6c396212189db6bb681fabf8c9d47b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 15 Jun 2023 00:39:56 GMT
ADD file:1c25b0be52aae22767603d9404fb777e27c5dd1bcd627221aac7517ac1bce1e3 in / 
# Thu, 15 Jun 2023 00:39:57 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 04:28:32 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 15 Jun 2023 04:28:32 GMT
ENV LANG=en_US.utf8
# Thu, 15 Jun 2023 04:28:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 15 Jun 2023 04:51:12 GMT
ENV PG_MAJOR=13
# Thu, 15 Jun 2023 04:51:12 GMT
ENV PG_VERSION=13.11
# Thu, 15 Jun 2023 04:51:13 GMT
ENV PG_SHA256=4992ff647203566b670d4e54dc5317499a26856c93576d0ea951bdf6bee50bfb
# Thu, 15 Jun 2023 04:51:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 15 Jun 2023 04:54:29 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Jun 2023 04:54:33 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Jun 2023 04:54:34 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Thu, 15 Jun 2023 04:54:34 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Jun 2023 04:54:35 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Thu, 15 Jun 2023 04:54:35 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Jun 2023 04:54:35 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Thu, 15 Jun 2023 04:54:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 04:54:36 GMT
STOPSIGNAL SIGINT
# Thu, 15 Jun 2023 04:54:36 GMT
EXPOSE 5432
# Thu, 15 Jun 2023 04:54:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8436307590cda5ccded8a952bb1d66684f8700d07029527293dd695eac6fabc9`  
		Last Modified: Thu, 15 Jun 2023 00:40:39 GMT  
		Size: 3.4 MB (3389905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff08446776d1583097fd1de191ffd52d0955341c2a81b6788d62261e150fa8d4`  
		Last Modified: Thu, 15 Jun 2023 05:10:23 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a81ed607664a47cc73540ac2f13efd84343e75b1a3f7507406eb99e1f883054`  
		Last Modified: Thu, 15 Jun 2023 05:10:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc6289875016ecc98d413cc97581de6e3fd792c01ae73280a5610d570a28ec8`  
		Last Modified: Thu, 15 Jun 2023 05:14:13 GMT  
		Size: 94.3 MB (94348938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc6fc9fbf2b0566c011ead33c2d66ebd1ce35122ffa5533dcd498b71fb2e76b`  
		Last Modified: Thu, 15 Jun 2023 05:13:51 GMT  
		Size: 9.0 KB (9027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e97fd4ef7541905134cc7c2a802ed0ef0e850d503eae750490c133eaad66d17`  
		Last Modified: Thu, 15 Jun 2023 05:13:51 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9963fce7f5a11456e846f93c92534c619a67786f6983e95a0443598119c8522c`  
		Last Modified: Thu, 15 Jun 2023 05:13:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee006f9ec273f5a41b64dbf3cc6b7970d6952f157e7e959ea9e45136b0db361d`  
		Last Modified: Thu, 15 Jun 2023 05:13:51 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine3.17` - linux; s390x

```console
$ docker pull postgres@sha256:9ac80e6b1b050f108b43e8453fe750d27fabc2d127e924ff48ef81ffe89fa8ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94772185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3d9aa703b002246e1995f95449ddbccbe89b3a7d3b2760596b7dc93cee96ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 29 Mar 2023 17:41:57 GMT
ADD file:675ad8acf4b076e34aeeba26dd482be7640df5912b1ec5e3183b7eb69c01e83e in / 
# Wed, 29 Mar 2023 17:41:57 GMT
CMD ["/bin/sh"]
# Fri, 19 May 2023 17:50:33 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 19 May 2023 17:50:33 GMT
ENV LANG=en_US.utf8
# Fri, 19 May 2023 17:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 19 May 2023 18:01:27 GMT
ENV PG_MAJOR=13
# Fri, 19 May 2023 18:01:27 GMT
ENV PG_VERSION=13.11
# Fri, 19 May 2023 18:01:27 GMT
ENV PG_SHA256=4992ff647203566b670d4e54dc5317499a26856c93576d0ea951bdf6bee50bfb
# Fri, 19 May 2023 18:01:27 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 19 May 2023 18:03:45 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 19 May 2023 18:03:48 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 19 May 2023 18:03:48 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Fri, 19 May 2023 18:03:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 19 May 2023 18:03:49 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Fri, 19 May 2023 18:03:49 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 19 May 2023 18:03:49 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Fri, 19 May 2023 18:03:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 May 2023 18:03:49 GMT
STOPSIGNAL SIGINT
# Fri, 19 May 2023 18:03:49 GMT
EXPOSE 5432
# Fri, 19 May 2023 18:03:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a76f78d8854217635d8049ec8501edb806f961e72989cfff8503982e6ff2579d`  
		Last Modified: Wed, 29 Mar 2023 17:42:31 GMT  
		Size: 3.2 MB (3175187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9265341bd5b8527e6bb9a1dba463af9c1c83742e3612106346ff1a44fe3c49a1`  
		Last Modified: Fri, 19 May 2023 18:14:49 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b21b24a1f2bba83d3e5a9d5cb92ac86101bd9ee00871c8782493a717c2077b`  
		Last Modified: Fri, 19 May 2023 18:14:49 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74873c2879cbc17c731879013c514e57b2e68be03617b6a1886bac4b73ef3210`  
		Last Modified: Fri, 19 May 2023 18:16:18 GMT  
		Size: 91.6 MB (91581390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f38426b95c675927d5c563f00824de2da347e17b6184ca157dce8633be1b4dc`  
		Last Modified: Fri, 19 May 2023 18:16:07 GMT  
		Size: 9.0 KB (9026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486a0eb57b903f1ec2dfbf2aedb6995a242c80a2d36ad7d944dd59273d3489f6`  
		Last Modified: Fri, 19 May 2023 18:16:07 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f099befb7923d2f8abd0610eb8a9d3dd51094c8b42d912d8a8229ab8256ef41`  
		Last Modified: Fri, 19 May 2023 18:16:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8e1317e8c8b14f13f05b3b9776c11adcffd503865e642c99ccacef7e76281b`  
		Last Modified: Fri, 19 May 2023 18:16:07 GMT  
		Size: 4.8 KB (4793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
