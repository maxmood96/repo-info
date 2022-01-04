## `postgres:9-alpine`

```console
$ docker pull postgres@sha256:8342bcb43446694428ec6594e72e4299692854f0fc3aca090b0ab46f4c7f32a1
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

### `postgres:9-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:84e6f6c787244669a874be441f44a64256a7f1d08d49505bd03cfc3c687b6cfd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20585569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cbcabaa33be3767f6617de9fd569a028f42cc8be1bb0a7ed2dafc233670497a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:59:34 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 30 Nov 2021 04:59:34 GMT
ENV LANG=en_US.utf8
# Tue, 30 Nov 2021 04:59:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 30 Nov 2021 05:40:27 GMT
ENV PG_MAJOR=9.6
# Tue, 30 Nov 2021 05:40:27 GMT
ENV PG_VERSION=9.6.24
# Tue, 30 Nov 2021 05:40:28 GMT
ENV PG_SHA256=aeb7a196be3ebed1a7476ef565f39722187c108dd47da7489be9c4fcae982ace
# Tue, 30 Nov 2021 05:46:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-utils 		perl-ipc-run 		perl-dev 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 30 Nov 2021 05:46:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 30 Nov 2021 05:46:42 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 30 Nov 2021 05:46:42 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Nov 2021 05:46:43 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 30 Nov 2021 05:46:43 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jan 2022 01:20:51 GMT
COPY file:cda82b5709f66a90b6babd661411ef1a87d0c9eeeae48253ec3248341658f54d in /usr/local/bin/ 
# Tue, 04 Jan 2022 01:20:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 04 Jan 2022 01:20:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jan 2022 01:20:52 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jan 2022 01:20:52 GMT
EXPOSE 5432
# Tue, 04 Jan 2022 01:20:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50e01d57241cf7ef93a91060f5eb0b895a4b443f20dc1ce5e77d441184a6dc2`  
		Last Modified: Tue, 30 Nov 2021 05:48:55 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0646b0f1eadaf0cd3fdb4c4490a69c4c7aed9b7ae10b24eb9005c59aa0b6e57`  
		Last Modified: Tue, 30 Nov 2021 05:48:55 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912227b294eef53a0b3b659a249ff5d362559c5dd7fd8bd7fa4f77e9dc23baae`  
		Last Modified: Tue, 30 Nov 2021 05:55:16 GMT  
		Size: 17.8 MB (17753003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696b75eaa88eb8c35e16fe0800e0ea481a51be17ab42ab689ce486f632a51c3a`  
		Last Modified: Tue, 30 Nov 2021 05:55:10 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d83746bb80be252099e8bdc0da91fb48140d0433e3d15eaaefebedf6b69461d`  
		Last Modified: Tue, 30 Nov 2021 05:55:10 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a431a2253cd02965829d563f6181cf8d6e756f31dfe04ceb340edc589d82920`  
		Last Modified: Tue, 30 Nov 2021 05:55:10 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ff05c047601c3cedb7dd5d6a494b9648602a7bb7180fcb04b74e79ae67104b`  
		Last Modified: Tue, 04 Jan 2022 01:25:42 GMT  
		Size: 4.7 KB (4722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587cf5e11ca1cd63b17de52d0ca5c065355f2301954bf46e275a2ba93216735e`  
		Last Modified: Tue, 04 Jan 2022 01:25:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:143356e2b080defa3adc1dfbafff70b82aaaff26835e32eb49ae426abc267288
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19977633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa7da6dfc2510c9dbaae59d997d3a488369e8f85606c3ab3b6a76a050fc11f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:39:17 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 30 Nov 2021 04:39:18 GMT
ENV LANG=en_US.utf8
# Tue, 30 Nov 2021 04:39:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 30 Nov 2021 05:06:26 GMT
ENV PG_MAJOR=9.6
# Tue, 30 Nov 2021 05:06:27 GMT
ENV PG_VERSION=9.6.24
# Tue, 30 Nov 2021 05:06:27 GMT
ENV PG_SHA256=aeb7a196be3ebed1a7476ef565f39722187c108dd47da7489be9c4fcae982ace
# Tue, 30 Nov 2021 05:12:31 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-utils 		perl-ipc-run 		perl-dev 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 30 Nov 2021 05:12:33 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 30 Nov 2021 05:12:35 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 30 Nov 2021 05:12:35 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Nov 2021 05:12:37 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 30 Nov 2021 05:12:37 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jan 2022 01:51:06 GMT
COPY file:cda82b5709f66a90b6babd661411ef1a87d0c9eeeae48253ec3248341658f54d in /usr/local/bin/ 
# Tue, 04 Jan 2022 01:51:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 04 Jan 2022 01:51:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jan 2022 01:51:08 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jan 2022 01:51:08 GMT
EXPOSE 5432
# Tue, 04 Jan 2022 01:51:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a865398e355d4d5f58fd1b16748daf1827598bdf1ba26c1d38fa7c8370d6705c`  
		Last Modified: Tue, 30 Nov 2021 05:15:02 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d879fc486c1bcf6d31fd2a8a5a4bc14acf4cc6f2d73e99dbf611ea8532bf4685`  
		Last Modified: Tue, 30 Nov 2021 05:15:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ca90726bd903fe90838d5a7ba475a53e8833150e130cbba86581d9a1c55f4f`  
		Last Modified: Tue, 30 Nov 2021 05:20:13 GMT  
		Size: 17.3 MB (17332047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2549e6a55626b4d0a845a0feb2d12fb52b0a41466b58a5de7ff53fb52517885`  
		Last Modified: Tue, 30 Nov 2021 05:20:00 GMT  
		Size: 7.5 KB (7530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a618fe02169697e7718a6b2f8b1eda534205faa6d3eac6ed21aa8aedf1417aa9`  
		Last Modified: Tue, 30 Nov 2021 05:19:59 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d10594da91485d3abab8a91bf902c44227e5d476902ce2734ac19c33caaee6e`  
		Last Modified: Tue, 30 Nov 2021 05:19:59 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc8c704cbc309f6323e666a4c1570fa46af8df2a5b3dc2b5098f1fc30e58823`  
		Last Modified: Tue, 04 Jan 2022 01:55:17 GMT  
		Size: 4.7 KB (4726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56dbd20fc65c706b53e7a359f0df19cc9abcc61e6a7f64e4e7022911eb83ac33`  
		Last Modified: Tue, 04 Jan 2022 01:55:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:02ac76c9710d4fdedc873fea10b6561e94b1793763ac0d931db61ccabd363e2a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18913921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4566f21f457adb68332f87d7b435655d58f4763500b8629ebd36562af785add5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 07:45:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 30 Nov 2021 07:45:15 GMT
ENV LANG=en_US.utf8
# Tue, 30 Nov 2021 07:45:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 30 Nov 2021 11:58:30 GMT
ENV PG_MAJOR=9.6
# Tue, 30 Nov 2021 11:58:30 GMT
ENV PG_VERSION=9.6.24
# Tue, 30 Nov 2021 11:58:31 GMT
ENV PG_SHA256=aeb7a196be3ebed1a7476ef565f39722187c108dd47da7489be9c4fcae982ace
# Tue, 30 Nov 2021 12:04:12 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-utils 		perl-ipc-run 		perl-dev 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 30 Nov 2021 12:04:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 30 Nov 2021 12:04:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 30 Nov 2021 12:04:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Nov 2021 12:04:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 30 Nov 2021 12:04:18 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jan 2022 01:01:53 GMT
COPY file:cda82b5709f66a90b6babd661411ef1a87d0c9eeeae48253ec3248341658f54d in /usr/local/bin/ 
# Tue, 04 Jan 2022 01:01:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 04 Jan 2022 01:01:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jan 2022 01:01:55 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jan 2022 01:01:56 GMT
EXPOSE 5432
# Tue, 04 Jan 2022 01:01:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f681d006162b865bd7dca8476d129c7fa1193b246ad8a598d27eb28769a6ac`  
		Last Modified: Tue, 30 Nov 2021 12:10:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74eb577cd41aefd27e490e1cbe04812996920ee2af42f358c659d1bb8a40230`  
		Last Modified: Tue, 30 Nov 2021 12:10:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6baeb1c8878d3e1abab3f69f4ca42be05b18fe095a6fae2385c8fcdbaa922a`  
		Last Modified: Tue, 30 Nov 2021 12:22:41 GMT  
		Size: 16.5 MB (16464996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18116710e91369a1e7a8a3affdfa98a688a5c1791d704cfc3fc66347993ffd17`  
		Last Modified: Tue, 30 Nov 2021 12:22:29 GMT  
		Size: 7.5 KB (7526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c45ee8313f8139371731d747bf0e856e6214e69f1caad563ec314b7571fcf5`  
		Last Modified: Tue, 30 Nov 2021 12:22:29 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ef760388ab0018419c5bc807ee6026473ae9d988a583a26a77cc7797344739`  
		Last Modified: Tue, 30 Nov 2021 12:22:29 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd13a0e3cb2d3f4461998626d54798184f40bd9b3f945819c9acc9afc6c67d01`  
		Last Modified: Tue, 04 Jan 2022 01:11:50 GMT  
		Size: 4.7 KB (4728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd8dacdb3d700223082f2ab5acf473c8895191769dee3fd406f652a7b59c415`  
		Last Modified: Tue, 04 Jan 2022 01:11:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:2cde527ea258b21a2966bd18a604b320bc89b47f378ca75cb57596c5a2d4f2c5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20387196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a368e0e3b16fec068853171da17fb3a1b882a1bf09a57234c7ecb12822b44462`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:27:18 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 30 Nov 2021 04:27:19 GMT
ENV LANG=en_US.utf8
# Tue, 30 Nov 2021 04:27:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 30 Nov 2021 05:16:00 GMT
ENV PG_MAJOR=9.6
# Tue, 30 Nov 2021 05:16:01 GMT
ENV PG_VERSION=9.6.24
# Tue, 30 Nov 2021 05:16:02 GMT
ENV PG_SHA256=aeb7a196be3ebed1a7476ef565f39722187c108dd47da7489be9c4fcae982ace
# Tue, 30 Nov 2021 05:19:29 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-utils 		perl-ipc-run 		perl-dev 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 30 Nov 2021 05:19:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 30 Nov 2021 05:19:31 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 30 Nov 2021 05:19:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Nov 2021 05:19:33 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 30 Nov 2021 05:19:34 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jan 2022 01:42:44 GMT
COPY file:cda82b5709f66a90b6babd661411ef1a87d0c9eeeae48253ec3248341658f54d in /usr/local/bin/ 
# Tue, 04 Jan 2022 01:42:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 04 Jan 2022 01:42:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jan 2022 01:42:46 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jan 2022 01:42:47 GMT
EXPOSE 5432
# Tue, 04 Jan 2022 01:42:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995a68b04f2b01f2160f500ef732a967a427af5da712fac9029eeecbc80af73d`  
		Last Modified: Tue, 30 Nov 2021 05:22:34 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a8bdf2ee5e8b95fdba44140b8595c955b8639595bcf5c0f15841330176d8e5`  
		Last Modified: Tue, 30 Nov 2021 05:22:35 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff563b142cc67b968bc4cb647edf869ffac82a4b6aff5bc9f822a500026e5d1`  
		Last Modified: Tue, 30 Nov 2021 05:28:48 GMT  
		Size: 17.7 MB (17657714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03921e76b2a1a895c6097b1267bfde824dd5b9e240e0ad265f8e730d89deeb2a`  
		Last Modified: Tue, 30 Nov 2021 05:28:43 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b5f7f3ef23a5445182cc7e701a6cf368db092c4fd0577b40390ad24cd43a96`  
		Last Modified: Tue, 30 Nov 2021 05:28:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da25e6f3bb53710ee80fd03f776cbe06da5aacc8ccd081594ea306ce4a96346`  
		Last Modified: Tue, 30 Nov 2021 05:28:43 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f86e4083ca19aec15f65363525ffd22de841204496855737b2c0d9a282c692`  
		Last Modified: Tue, 04 Jan 2022 01:49:06 GMT  
		Size: 4.7 KB (4724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2a0b3f05cc73880b0ffd5918ab817e0111f512ad010c5bccc4a254c85004db`  
		Last Modified: Tue, 04 Jan 2022 01:49:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; 386

```console
$ docker pull postgres@sha256:3458a6d25b3b2c1867e3b62813fbad71bf868af3104e607c6fd6cfc64748aa50
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21127618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e03ad321c4a131d01b748c7d2aba048118a31c7204d116be908e1d303a7a4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 24 Nov 2021 20:53:48 GMT
ADD file:b9a17131c440053f2f67e127b447645f25fd7de2d6caca42f569cafab6291855 in / 
# Wed, 24 Nov 2021 20:53:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 02:41:28 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 30 Nov 2021 02:41:28 GMT
ENV LANG=en_US.utf8
# Tue, 30 Nov 2021 02:41:29 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 30 Nov 2021 04:34:49 GMT
ENV PG_MAJOR=9.6
# Tue, 30 Nov 2021 04:34:50 GMT
ENV PG_VERSION=9.6.24
# Tue, 30 Nov 2021 04:34:50 GMT
ENV PG_SHA256=aeb7a196be3ebed1a7476ef565f39722187c108dd47da7489be9c4fcae982ace
# Tue, 30 Nov 2021 04:40:04 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-utils 		perl-ipc-run 		perl-dev 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 30 Nov 2021 04:40:05 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 30 Nov 2021 04:40:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 30 Nov 2021 04:40:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Nov 2021 04:40:08 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 30 Nov 2021 04:40:08 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jan 2022 01:40:36 GMT
COPY file:cda82b5709f66a90b6babd661411ef1a87d0c9eeeae48253ec3248341658f54d in /usr/local/bin/ 
# Tue, 04 Jan 2022 01:40:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 04 Jan 2022 01:40:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jan 2022 01:40:37 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jan 2022 01:40:38 GMT
EXPOSE 5432
# Tue, 04 Jan 2022 01:40:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e6889e0d66307a4b916fc844f2dcbc03245c63bc4189dd3e88126d9dcf2f9231`  
		Last Modified: Wed, 24 Nov 2021 20:54:48 GMT  
		Size: 2.8 MB (2827117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af56146d51f459d9baa843fcf88ab0b80c1c9de99248bc2163f19197ba95d05`  
		Last Modified: Tue, 30 Nov 2021 04:43:41 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a14412d0e45405abe51e591c8467d465e5f91db0600bf8b9120d9c6f15217c`  
		Last Modified: Tue, 30 Nov 2021 04:43:41 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036c8d88755da68775d230879ce2fb3dc8d2e03352afb0dbc0900f78999a163c`  
		Last Modified: Tue, 30 Nov 2021 04:51:29 GMT  
		Size: 18.3 MB (18286340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafd363ea4227d662050375308d13cf0e6030aed1a13c29ca40ddcfa157e82bd`  
		Last Modified: Tue, 30 Nov 2021 04:51:22 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7519af586b1d69f4deb8da0a2ed79ddc93d74e3fdd6cedb94ca3b47535bbfb6`  
		Last Modified: Tue, 30 Nov 2021 04:51:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82324004fee0851745526ea8a5a75140dcbe162f66910e4706c7b98eb1750e6`  
		Last Modified: Tue, 30 Nov 2021 04:51:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea91e958919e487f87d9e91b2df68b87045e9fdff81cfc506361691bbf831d7`  
		Last Modified: Tue, 04 Jan 2022 01:47:21 GMT  
		Size: 4.7 KB (4727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd3aedd575b1d527676cdd95b108ee95f0c95ea801e6488e5bed6afb6a4edbe`  
		Last Modified: Tue, 04 Jan 2022 01:47:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:808e41bb13b7bfcc4c9c46a0b70eb03a30a792d0339b00dc7bbde174643cb0e7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 MB (21727901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf82ce5949eb7a6e4836ff2f3341441ea9e5b9c1923a74c94215888240c389a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:26:49 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 30 Nov 2021 04:26:53 GMT
ENV LANG=en_US.utf8
# Tue, 30 Nov 2021 04:27:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 30 Nov 2021 05:02:30 GMT
ENV PG_MAJOR=9.6
# Tue, 30 Nov 2021 05:02:32 GMT
ENV PG_VERSION=9.6.24
# Tue, 30 Nov 2021 05:02:35 GMT
ENV PG_SHA256=aeb7a196be3ebed1a7476ef565f39722187c108dd47da7489be9c4fcae982ace
# Tue, 30 Nov 2021 05:07:02 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-utils 		perl-ipc-run 		perl-dev 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 30 Nov 2021 05:07:12 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 30 Nov 2021 05:07:21 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 30 Nov 2021 05:07:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Nov 2021 05:07:30 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 30 Nov 2021 05:07:32 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jan 2022 01:20:32 GMT
COPY file:cda82b5709f66a90b6babd661411ef1a87d0c9eeeae48253ec3248341658f54d in /usr/local/bin/ 
# Tue, 04 Jan 2022 01:20:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 04 Jan 2022 01:20:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jan 2022 01:20:42 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jan 2022 01:20:44 GMT
EXPOSE 5432
# Tue, 04 Jan 2022 01:20:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21143ce0a44ab602b12471d2a1cf95c5dcbc9d805bd8ede00e2766f24d295b5`  
		Last Modified: Tue, 30 Nov 2021 05:10:51 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c45529781f9e932a9022851fca78ba53022920657aa14e0479b195cac40189`  
		Last Modified: Tue, 30 Nov 2021 05:10:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4b0422694f624540e0e4af934b81b1daec99d7cf52accffa195fae452f654d`  
		Last Modified: Tue, 30 Nov 2021 05:16:39 GMT  
		Size: 18.9 MB (18898956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6aeb049e740133cde6c6e215d481785e35130517ea79f7ad6996f73ec5a485b`  
		Last Modified: Tue, 30 Nov 2021 05:16:32 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b0833d853f28072565f53343077d871a96442c16710cac4d4dd1cf7ec87079`  
		Last Modified: Tue, 30 Nov 2021 05:16:32 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723d590965e15c6433a0926b6da4fceb6334afb05784386f10fe0d9ef04915b4`  
		Last Modified: Tue, 30 Nov 2021 05:16:31 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d829a2c30492b376199633a33f488bc05e40d6a238fe0eff530ab211cd3c90`  
		Last Modified: Tue, 04 Jan 2022 01:26:11 GMT  
		Size: 4.7 KB (4727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909505ad0b91b28ae5d4fbe2df66274405a46eb3548f8cbdf14f44ed304ee019`  
		Last Modified: Tue, 04 Jan 2022 01:24:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:fbd158ea680e9d7b3bc430366fffe2d1f3bc9653075131ce79f2537695be77d1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20572613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3144119176d208fce4917dea42ca5828015a944a36fead399fd6e40073f9fb66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 08:50:09 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 30 Nov 2021 08:50:09 GMT
ENV LANG=en_US.utf8
# Tue, 30 Nov 2021 08:50:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 30 Nov 2021 09:41:37 GMT
ENV PG_MAJOR=9.6
# Tue, 30 Nov 2021 09:41:38 GMT
ENV PG_VERSION=9.6.24
# Tue, 30 Nov 2021 09:41:38 GMT
ENV PG_SHA256=aeb7a196be3ebed1a7476ef565f39722187c108dd47da7489be9c4fcae982ace
# Tue, 30 Nov 2021 09:44:19 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-utils 		perl-ipc-run 		perl-dev 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 30 Nov 2021 09:44:21 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 30 Nov 2021 09:44:21 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 30 Nov 2021 09:44:21 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Nov 2021 09:44:22 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 30 Nov 2021 09:44:22 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jan 2022 01:43:09 GMT
COPY file:cda82b5709f66a90b6babd661411ef1a87d0c9eeeae48253ec3248341658f54d in /usr/local/bin/ 
# Tue, 04 Jan 2022 01:43:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 04 Jan 2022 01:43:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jan 2022 01:43:10 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jan 2022 01:43:10 GMT
EXPOSE 5432
# Tue, 04 Jan 2022 01:43:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96844042cfb587d09e525bf6890e267412ad5971e27ece4faa02e82f6fda3c87`  
		Last Modified: Tue, 30 Nov 2021 09:46:44 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826ee6a78ec06ec30a73acc9c0f2337f744b77da2931a6e0c1d3efb35d76cfe6`  
		Last Modified: Tue, 30 Nov 2021 09:46:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2130432d59871cd32d2f0a3ec3d6fc9c3351b36f36c4bda5f694d28be3a27108`  
		Last Modified: Tue, 30 Nov 2021 09:49:57 GMT  
		Size: 18.0 MB (17952512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd80ddfe1c4fafea7683578ad48f799f23967bfdb1d1e06b581c46a6e494c78`  
		Last Modified: Tue, 30 Nov 2021 09:49:53 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c7da98d17656b665d1bba3bb2af967155ffa4074a01e1dfb598651ef5d5886`  
		Last Modified: Tue, 30 Nov 2021 09:49:53 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9b8b8239574fd49c2d0a5d26cca9c58e6dded59b89f57eea3111e71f137501`  
		Last Modified: Tue, 30 Nov 2021 09:49:53 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c939b3e3c75605b025ea00ea6d30b739471a0bebc6da33776a9a8e0e8e80cb4e`  
		Last Modified: Tue, 04 Jan 2022 01:47:07 GMT  
		Size: 4.7 KB (4723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dfaa48e2f39ba327d6589b24d00f70715bf3f7ae1168af719af16738d61a3f`  
		Last Modified: Tue, 04 Jan 2022 01:47:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
