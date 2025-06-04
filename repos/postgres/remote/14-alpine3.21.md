## `postgres:14-alpine3.21`

```console
$ docker pull postgres@sha256:1e68db130836f266d4af4b754c39380cc8aa52e65c3e18dba7b647633f118b73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:14-alpine3.21` - linux; amd64

```console
$ docker pull postgres@sha256:71db047043cb783eefadb0164cbaa72e21efcafd7425029f302e9a17d6034264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108261518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5089e2619ce05e7d56b139cc2c91a77f82462e4fc8f08118534abed75ad09680`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV LANG=en_US.utf8
# Fri, 30 May 2025 21:09:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_MAJOR=14
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_VERSION=14.18
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_SHA256=83ab29d6bfc3dc58b2ed3c664114fdfbeb6a0450c4b8d7fa69aee91e3ca14f8e
# Fri, 30 May 2025 21:09:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 30 May 2025 21:09:41 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 30 May 2025 21:09:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 21:09:41 GMT
STOPSIGNAL SIGINT
# Fri, 30 May 2025 21:09:41 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 30 May 2025 21:09:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f61ae5473a78bb831dfb0fe04880fe75eee0b852c6017bd6f47aafba0d13f3`  
		Last Modified: Tue, 03 Jun 2025 13:47:23 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d748d3741aa5746b7fb82543a8c0c8a797cccce917e91524ce959be9143b81`  
		Last Modified: Tue, 03 Jun 2025 13:47:24 GMT  
		Size: 1.1 MB (1120319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daeb2f7586cc2a4a03f3ef3b92b18e13b5f58b0e11991f3046e61a026fd35710`  
		Last Modified: Tue, 03 Jun 2025 13:47:23 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf39778e21380d45e2818b28f7d679c0bc04c835a62f4024128eed80a96a9493`  
		Last Modified: Tue, 03 Jun 2025 13:47:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb2933509ffa4e9195d8b6e270b4333a5c38e6b08933a4ec7b65de38438aa79`  
		Last Modified: Tue, 03 Jun 2025 13:47:32 GMT  
		Size: 103.5 MB (103482532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e30b47ebb67f1f3a41e483d7dd3660020270ad3af9bc55f742deeaf8b4acfaa`  
		Last Modified: Tue, 03 Jun 2025 13:47:25 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9eb1e3c7d7ce2451faec9a382f759090c72585ad1606bcf2a8dcc4956fae069`  
		Last Modified: Tue, 03 Jun 2025 13:47:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6903a024b65d8d4df95ee041b91390de0df4cdbcca05609fe483118510e0381a`  
		Last Modified: Tue, 03 Jun 2025 13:47:28 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a68224b7e1fa5d4bdd9207bca0e2e6dfcc721443694d86fa58c6a4dbc6f880d`  
		Last Modified: Tue, 03 Jun 2025 13:47:29 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341f16925aa5e75724d8b1501827368a32fd80021747cb79daa25bdb9b2b194d`  
		Last Modified: Tue, 03 Jun 2025 13:47:30 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:49ed1f1a8e4184f55b7ee09b9ceb067c69f3f58d7e0ae54fad5068230d57462b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.1 KB (642132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eabf231a5478709d6789348276b7ca7d5b7c71849710971b55621260a16d00d`

```dockerfile
```

-	Layers:
	-	`sha256:34891526358a018413c7e8013e4f1ef1a7328c2d90268f49d64ed9dc86ba7988`  
		Last Modified: Tue, 03 Jun 2025 23:00:32 GMT  
		Size: 598.7 KB (598700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0c47b12362242fda1dc3d9051788e15130fee8005f8ec5a631ddfc5c50647db`  
		Last Modified: Tue, 03 Jun 2025 23:00:33 GMT  
		Size: 43.4 KB (43432 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.21` - linux; arm variant v6

```console
$ docker pull postgres@sha256:c29da4c34af65b2939012d15f79d71e7192453122b0c0e2b8f57b07b7863c4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87885675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674df8af965a003c8f9adcbdef4b45c26fb43a0d62d6964a3edd6c8ba59682b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV LANG=en_US.utf8
# Fri, 30 May 2025 21:09:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_MAJOR=14
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_VERSION=14.18
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_SHA256=83ab29d6bfc3dc58b2ed3c664114fdfbeb6a0450c4b8d7fa69aee91e3ca14f8e
# Fri, 30 May 2025 21:09:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 30 May 2025 21:09:41 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 30 May 2025 21:09:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 21:09:41 GMT
STOPSIGNAL SIGINT
# Fri, 30 May 2025 21:09:41 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 30 May 2025 21:09:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e8cc19bee9308afcbf52843a00e4ef4972c49cf21acd9b92368cecf528ff49`  
		Last Modified: Sat, 15 Feb 2025 00:09:03 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781627176b8f9e10a830d9e3a634776cd0db6531992b444881c58b767652e146`  
		Last Modified: Sat, 15 Feb 2025 00:09:03 GMT  
		Size: 1.1 MB (1086598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5c66ed96baf47284abdd1941a68e679209bcd67c5115885f337bd99a0c6008`  
		Last Modified: Sat, 15 Feb 2025 00:09:03 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221e19b745e47706571cde1555189229d670f7c69c24c2b57e6260be58b7045a`  
		Last Modified: Sat, 15 Feb 2025 00:09:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab47807a519c6ecd3a3ba1e67258cf375385bc7b4d19d84103346188b3492390`  
		Last Modified: Thu, 08 May 2025 19:39:31 GMT  
		Size: 83.4 MB (83417917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933d867cf137390be3197519a7a4c37cedefda4a5bd1b12a65e35c46a80c1bcc`  
		Last Modified: Thu, 08 May 2025 19:39:20 GMT  
		Size: 9.2 KB (9206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6d68d16f4a7c6053ebfb93bc9e07f85c7b059d97185163f4d6917298e8f07a`  
		Last Modified: Thu, 08 May 2025 19:39:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba7f6a15e878c466e4ddf3b308fbf2721e118a2f7c830df7f359b6b6a0c5813`  
		Last Modified: Thu, 08 May 2025 19:39:20 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2117bd5c860c8b43ece564a7d2237d7b8de62534887b5072773ed854d1c1719`  
		Last Modified: Thu, 08 May 2025 19:39:21 GMT  
		Size: 5.5 KB (5474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f0662e69fdccc4104b3623969f9864bc410548e22f55f953d68783b19b203d`  
		Last Modified: Tue, 03 Jun 2025 15:20:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:78b68f2c45dd48c71c868918d03c28901dc401e4f80d77d56d4bdf4ea637524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 KB (43375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826fa398d64a50704865e8f1fa9a1bb3f9deb242dd8c323890c3d48d86b45817`

```dockerfile
```

-	Layers:
	-	`sha256:9a4e0a2d45120250ced7a47fdd53a4306b895f14ffd999b2ea3fd6f61f491681`  
		Last Modified: Tue, 03 Jun 2025 23:00:34 GMT  
		Size: 43.4 KB (43375 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.21` - linux; arm variant v7

```console
$ docker pull postgres@sha256:1688a88f960db751b661ec371627566e00904af93cbee5634c126091a54d6e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83141396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9287d582eef0cf1ece268d15c40d19e306ddea5e21eb48c4e2dc3b82311de2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV LANG=en_US.utf8
# Fri, 30 May 2025 21:09:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_MAJOR=14
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_VERSION=14.18
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_SHA256=83ab29d6bfc3dc58b2ed3c664114fdfbeb6a0450c4b8d7fa69aee91e3ca14f8e
# Fri, 30 May 2025 21:09:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 30 May 2025 21:09:41 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 30 May 2025 21:09:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 21:09:41 GMT
STOPSIGNAL SIGINT
# Fri, 30 May 2025 21:09:41 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 30 May 2025 21:09:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ada47321bd0e89157bae4052aa7de0b68f59e22e5aa8ed76cb27a9a4fb2758b`  
		Last Modified: Thu, 08 May 2025 19:52:10 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997421b050761e5bc8fffaa3538a99a0dfde2e21a4b3c0d5f0432f97e3b5127d`  
		Last Modified: Thu, 08 May 2025 19:52:12 GMT  
		Size: 1.1 MB (1086588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3ebd6a73bb383b8af8f2740ed00d938ad77aded3653a6c82feb078c4df2e9d`  
		Last Modified: Thu, 08 May 2025 20:29:06 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f44772b8b361b4f64d07c3deb45db2f43c43f540d73e8bba67c33366661daf`  
		Last Modified: Thu, 08 May 2025 20:29:07 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fee94cce7e3ae168cc2f87d02d5685928aa95346092268c49788d17d6e7169`  
		Last Modified: Thu, 08 May 2025 21:45:57 GMT  
		Size: 78.9 MB (78940244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7419b82c3c0741fcb4596ea68e356606d46739d9074cf03fdfabde517308479d`  
		Last Modified: Thu, 08 May 2025 21:45:29 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854a68fc5c60aeaa2ca5a0db98b07e519bc68834d377ec7d86d71de411ba58d3`  
		Last Modified: Tue, 03 Jun 2025 13:36:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f835344c881e1e590cf55fe28376b222a6b9a9662465156d8cab092635c51dcb`  
		Last Modified: Tue, 03 Jun 2025 13:45:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf8b6306943c7097e192624c7fd9582751ef06ec0d8dd7475e400c720ce666e`  
		Last Modified: Tue, 03 Jun 2025 14:23:31 GMT  
		Size: 5.5 KB (5481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f2f3856ad8effad7970f166667a2240d2b2ce9c2f92fc347416f7debf6cfa7`  
		Last Modified: Tue, 03 Jun 2025 13:42:26 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:aef3588aad617c3110b85c37b4376bcc50ca7dc5a01e529bbcc30df825f4a70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.3 KB (642311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73aff810f848a825c5ec4d2604dd74f839eabeb6fc6b3a62f08d46a0e334f3a`

```dockerfile
```

-	Layers:
	-	`sha256:39c4d2fee050aa439b014bf5ec3bb1ca3439e3ce3f86cde652fc3c4af1f007f9`  
		Last Modified: Tue, 03 Jun 2025 23:00:37 GMT  
		Size: 598.7 KB (598720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:847551f501758eb814764e034e0bb7b5b54ba381e804ec78ca53c030ec9ea689`  
		Last Modified: Tue, 03 Jun 2025 23:00:38 GMT  
		Size: 43.6 KB (43591 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:89a63173a472edff1253b3746e7f7f0208047812f5ee7b186fb73fbad5acffea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104163433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d181583bcea794ff8753e65d2ab669331a4ec7e6b681e3278622c02acdd577f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV LANG=en_US.utf8
# Fri, 30 May 2025 21:09:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_MAJOR=14
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_VERSION=14.18
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_SHA256=83ab29d6bfc3dc58b2ed3c664114fdfbeb6a0450c4b8d7fa69aee91e3ca14f8e
# Fri, 30 May 2025 21:09:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 30 May 2025 21:09:41 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 30 May 2025 21:09:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 21:09:41 GMT
STOPSIGNAL SIGINT
# Fri, 30 May 2025 21:09:41 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 30 May 2025 21:09:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d03f0f2d53b2dbd9eb483b0627ccff77722b5cd779ea77b53d0c300329320e0`  
		Last Modified: Tue, 03 Jun 2025 13:33:42 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7253dfc6422805ac3c15fda3414a5e3fb679f89df5a9ecfb3b80db788b4e8dcf`  
		Last Modified: Tue, 03 Jun 2025 13:33:43 GMT  
		Size: 1.1 MB (1050058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61551669052ed2146736a74f619b32861f7a06f55d31c3d1549cee4f983ee9f5`  
		Last Modified: Tue, 03 Jun 2025 13:33:42 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c537ca15df89a2154ac1f300f5a2e2e67bb6ba6c7a2ac91204458317b7283e`  
		Last Modified: Tue, 03 Jun 2025 13:33:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b880c932ecac99271c5fa02b7fa216c2c95f97fec3e4f636487b4d5b3b4a4b`  
		Last Modified: Tue, 03 Jun 2025 14:23:33 GMT  
		Size: 99.1 MB (99103919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8282a167aadb5c4d5743c00b0c97d4e057c3162fb6fa0e42c0fa6381eef032cc`  
		Last Modified: Tue, 03 Jun 2025 13:53:00 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26373a48b6beaba81e08f557b21c727b0849bc9e2de4319816997b0dc2ec3125`  
		Last Modified: Tue, 03 Jun 2025 13:53:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714ef4581fcb207ec616861bc150411387cf8704591cfd7e1f8941e55ae02a07`  
		Last Modified: Tue, 03 Jun 2025 13:53:16 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725597a4a3126f34d83a88cc85dfe919dd944bbbb7f617555169f67c4a30375e`  
		Last Modified: Tue, 03 Jun 2025 13:53:21 GMT  
		Size: 5.5 KB (5472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cda8208c5a9744194634b646de9ccfe2efaa9e0232f6bde36df4042398e3b41`  
		Last Modified: Tue, 03 Jun 2025 13:53:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:ae1adf95f0b5d438a85f81e90a94ba8d042d9168a9f606a1250c4ed69a4d4d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.4 KB (642359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:106e8edc0407b4b8cc067fe2aff2843a5154dc088137dbe9d540455162b069c9`

```dockerfile
```

-	Layers:
	-	`sha256:52e870bfe1eb786839fa4398bc05000bbe6d6792f9f779d324b43cb3802cd4cf`  
		Last Modified: Tue, 03 Jun 2025 23:00:44 GMT  
		Size: 598.7 KB (598732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a137f26466df4028ef137453fc23bc39f2412562d9ae7784308c83969e8d7cc`  
		Last Modified: Tue, 03 Jun 2025 23:00:45 GMT  
		Size: 43.6 KB (43627 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.21` - linux; 386

```console
$ docker pull postgres@sha256:61639bcb28de1d3c8859250ba6725013b9d9da2916a690b7a7c4107b4599b928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114390137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965fa9c7664be15a5a2821ff7a8647b9ebc1e68751128f45e52483430b2c70f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV LANG=en_US.utf8
# Fri, 30 May 2025 21:09:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_MAJOR=14
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_VERSION=14.18
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_SHA256=83ab29d6bfc3dc58b2ed3c664114fdfbeb6a0450c4b8d7fa69aee91e3ca14f8e
# Fri, 30 May 2025 21:09:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 30 May 2025 21:09:41 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 30 May 2025 21:09:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 21:09:41 GMT
STOPSIGNAL SIGINT
# Fri, 30 May 2025 21:09:41 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 30 May 2025 21:09:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254218fc025635f6f2a3766180bfc2fb0f0152ed4fd355cdc34bf10703626894`  
		Last Modified: Tue, 03 Jun 2025 15:24:59 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ef4d15b6c5a1b71c1c705482c22beab80b643a691e789133788f57bf81e28b`  
		Last Modified: Tue, 03 Jun 2025 15:13:49 GMT  
		Size: 1.1 MB (1095260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76d76924a08bf75768d3ea456467c6b0df9be25df07d59bc53a6b2225454e26`  
		Last Modified: Tue, 03 Jun 2025 15:11:11 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0963cda8929c854308c0faf64956b870402045b11f39928ef7b231114b3cec6`  
		Last Modified: Tue, 03 Jun 2025 13:35:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1cc036977850f29d67176fa41226d235986d2d022c25d098f27f3ec344e942`  
		Last Modified: Tue, 03 Jun 2025 23:00:55 GMT  
		Size: 109.8 MB (109814834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2219af2a0cd4cbdfe4664d338976376144c277231176030fc9bafb8c23cf28`  
		Last Modified: Tue, 03 Jun 2025 15:24:12 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f768002c2033450ae0a4d5b18acc07639d4073200d3658e4389c5b199478d07`  
		Last Modified: Tue, 03 Jun 2025 15:36:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8974b8ae92c192c3c15fdedf6e466dd856f5d70ddae6927250c81baa358e81`  
		Last Modified: Tue, 03 Jun 2025 15:14:55 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c72f0bb9d912a325e6805b19f4ab1c3fb07a40ac42c12aa8b0fdccb0b160e2a`  
		Last Modified: Tue, 03 Jun 2025 15:18:43 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff461cf6fb00963d6a6b2f9c7fc278aceb7d5d25a07720fb4edd0824f5b6d8d5`  
		Last Modified: Tue, 03 Jun 2025 15:39:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:c1a27dc4eee37f7f171f7fe33fcb4eada4635613870d2a0fea43ffe6a4f56816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.1 KB (642080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c595102465851de6941be1dbd06cba2dd9c6b1ec7611c224fa2f78a453c7994c`

```dockerfile
```

-	Layers:
	-	`sha256:7f23a381d9abbbebcfec20d81d91bed6209841e5c9cb75f4941aa630788b414e`  
		Last Modified: Tue, 03 Jun 2025 23:00:51 GMT  
		Size: 598.7 KB (598685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d117a2d11e59e205b890e555c00ca6f695b8b3a64405936b94c686251dfd37e`  
		Last Modified: Tue, 03 Jun 2025 23:00:52 GMT  
		Size: 43.4 KB (43395 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.21` - linux; ppc64le

```console
$ docker pull postgres@sha256:2e8d99069120d0a766a8343cddd620620b518418b70b9d7ce8ce990ee5a7e5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91944426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f873b1943753e012a5cb54a5d3fdabcffd72494721719619f7db4d98f67feed3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV LANG=en_US.utf8
# Fri, 30 May 2025 21:09:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_MAJOR=14
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_VERSION=14.18
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_SHA256=83ab29d6bfc3dc58b2ed3c664114fdfbeb6a0450c4b8d7fa69aee91e3ca14f8e
# Fri, 30 May 2025 21:09:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 30 May 2025 21:09:41 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 30 May 2025 21:09:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 21:09:41 GMT
STOPSIGNAL SIGINT
# Fri, 30 May 2025 21:09:41 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 30 May 2025 21:09:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bbfa9887a7a761f236c6a62f7e2b1f9e06e4c49edc5445a1383c30a024f0fe`  
		Last Modified: Tue, 03 Jun 2025 15:33:09 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9154ad7d6d2b8215d6e5c17c7126973ef555179af7445e48dd15afbc769dab`  
		Last Modified: Tue, 03 Jun 2025 15:36:41 GMT  
		Size: 1.0 MB (1040368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccfd7f83cae351ae5c57d06c0bfe732186b0ac067d40dea3c3e0582e0fb1f0d`  
		Last Modified: Tue, 03 Jun 2025 15:19:03 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34f22e4bcd5ed37602675ddcd485f45a34c07d54f0c635ed4c95127597b99a1`  
		Last Modified: Tue, 03 Jun 2025 15:34:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74695d81f8bb8817089547af9dd56677a4d6205daaeaae7f44cdfbd2e1954cfb`  
		Last Modified: Tue, 03 Jun 2025 23:00:58 GMT  
		Size: 87.3 MB (87313289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dabd7ff41053684210d159354fb47bdc70c621944fd558c6b360274ee8ec0a`  
		Last Modified: Tue, 03 Jun 2025 15:40:07 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f084ec5c0c7b55dd59aa288108a6642c4909b4a7934a70e902abfa6c491e8c`  
		Last Modified: Tue, 03 Jun 2025 15:12:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266589245b90cc5334d2d9fd105e960067cb1281e7a0ebb154d7f584b351bcfe`  
		Last Modified: Tue, 03 Jun 2025 15:31:20 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcc03b986d18ba20296857851596bed3ee54ef587e99f3872592f19ecab40b1`  
		Last Modified: Tue, 03 Jun 2025 15:34:34 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cc1d0f9e45413ecbd4de13c037f066bcfbb0b7d0a64a398d753690c602328d`  
		Last Modified: Tue, 03 Jun 2025 15:41:42 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:c6f3058646017e0014e67f9dc29c7d7d8a9eefabbd378859b7e037f19c9a4c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.6 KB (638584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67183abe6069d524a47424e4ca457ffc56fd710313168f565025b55e6403c57a`

```dockerfile
```

-	Layers:
	-	`sha256:2860101edbb4f7e16c5ba323335073cb5863555885fc65ab3c0258f283f4e987`  
		Last Modified: Tue, 03 Jun 2025 23:01:00 GMT  
		Size: 595.1 KB (595109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dd91959a3e0e7d193944b4f3eebcc800e4f3410ef3a688e49de9951bb863164`  
		Last Modified: Tue, 03 Jun 2025 23:01:00 GMT  
		Size: 43.5 KB (43475 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.21` - linux; riscv64

```console
$ docker pull postgres@sha256:39bcef4cea9f19f7edb95cc36b19deb21c746d9b9b7c8fb030ba05d8d1157b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108156967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe41a5fd470de98ec0f0f4ec4161d7ac772d15e44d10d1ea88395a8d0a9ccdf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV LANG=en_US.utf8
# Fri, 30 May 2025 21:09:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_MAJOR=14
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_VERSION=14.18
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_SHA256=83ab29d6bfc3dc58b2ed3c664114fdfbeb6a0450c4b8d7fa69aee91e3ca14f8e
# Fri, 30 May 2025 21:09:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 30 May 2025 21:09:41 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 30 May 2025 21:09:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 21:09:41 GMT
STOPSIGNAL SIGINT
# Fri, 30 May 2025 21:09:41 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 30 May 2025 21:09:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51c32376219c4b96f02563de145a6dae5a45bd7698b8c7ca6f6da052086070b`  
		Last Modified: Fri, 09 May 2025 07:05:16 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8288dcf7d76e423837c7b22aaeabb3ffce916e0d4021374ef1030da4496878fb`  
		Last Modified: Fri, 09 May 2025 07:05:15 GMT  
		Size: 1.1 MB (1089773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6311d87ca151ab54043044f3c5d418b5c2b3511bcfb121e1b721202d992188d6`  
		Last Modified: Fri, 09 May 2025 08:55:23 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dda895e1bfe5751fb2792edcac1677d106f933fef00f14ea173cc99c103e50e`  
		Last Modified: Fri, 09 May 2025 08:55:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c328c04f967f7b21addd377ac665b92fd08457275b099102d963a543e2cddc8`  
		Last Modified: Fri, 09 May 2025 12:22:40 GMT  
		Size: 103.7 MB (103699310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33e00daf101bd9e8ad38a444056d72c53ff3b28231ee411cd09b359d06b73a9`  
		Last Modified: Fri, 09 May 2025 12:22:27 GMT  
		Size: 9.2 KB (9209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16db44f830154c148d7af24d3d536d2d15b01324fb62afcc1faf0ee289b05673`  
		Last Modified: Fri, 09 May 2025 12:22:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3990df6fcf6131dbc2a46ac4cc7261b0527e083215f2abb897f08bfd52cf5361`  
		Last Modified: Tue, 03 Jun 2025 23:01:01 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb1fd002fd111d70659466f57e31e40f0a76aed560954055227f6ee80723b8a`  
		Last Modified: Tue, 03 Jun 2025 23:01:02 GMT  
		Size: 5.5 KB (5478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61598cac889fe88ec038078beee76fafc2edca79a84a70cf2118a34d3648e2a5`  
		Last Modified: Tue, 03 Jun 2025 23:01:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:d9a7f995d774a2ea70a0fdd7af5838ba4c2eee855b26f5fcd83656ec208f9cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d73979a014d00a66b8a497708dfb8c50225498e6823405cea1bbbecbfc5efe8`

```dockerfile
```

-	Layers:
	-	`sha256:b0c6fb182256739026062c095e052a5a1793232758ae74ef3163271e9b14b7cb`  
		Last Modified: Tue, 03 Jun 2025 23:01:04 GMT  
		Size: 596.8 KB (596767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e35ffa5fbdb1365372f1ebc40e700c97c4d922db82e6ced9e58fbb9dae2f7290`  
		Last Modified: Tue, 03 Jun 2025 23:01:04 GMT  
		Size: 43.5 KB (43479 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.21` - linux; s390x

```console
$ docker pull postgres@sha256:8d04e24540529ec33aab18e56868491106a0611c9d57146070b0c65fbe16a630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116832832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9360c246f25de8ece5baa46133dba24541c541469cefa2d8bb3783149d9748a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV LANG=en_US.utf8
# Fri, 30 May 2025 21:09:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_MAJOR=14
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_VERSION=14.18
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_SHA256=83ab29d6bfc3dc58b2ed3c664114fdfbeb6a0450c4b8d7fa69aee91e3ca14f8e
# Fri, 30 May 2025 21:09:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 30 May 2025 21:09:41 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 30 May 2025 21:09:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 21:09:41 GMT
STOPSIGNAL SIGINT
# Fri, 30 May 2025 21:09:41 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 30 May 2025 21:09:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca41bc03c66f2db51ee7ccecf095cd1dba41a34a6d831663f4096bc1e32f4c79`  
		Last Modified: Tue, 03 Jun 2025 20:56:29 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e901e5ec0b869a1daf11fbf0499629c10c3fa04e7ffc3eb1336b6cb3d9dbb45`  
		Last Modified: Tue, 03 Jun 2025 20:56:31 GMT  
		Size: 1.1 MB (1084558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1691c9b6b947561e411eece26e4b4a00848bdc0c698d4a0a32a9f9eb44f0cc75`  
		Last Modified: Tue, 03 Jun 2025 22:58:52 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c68639e4c857b4d6683ede84c2f5c04f8e637ec33d7e45cbedcc2cac729924`  
		Last Modified: Tue, 03 Jun 2025 22:58:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f64df2daf1d71b7dff60256b4cc56d945189a9c732986ee4d54a3901be17947`  
		Last Modified: Tue, 03 Jun 2025 23:01:10 GMT  
		Size: 112.3 MB (112264279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891d757dba2614daf67535d18e7c38de468ba7ebbc0dca7650fabdf2f6df6364`  
		Last Modified: Tue, 03 Jun 2025 23:01:05 GMT  
		Size: 9.2 KB (9206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b35068673a98e45b2510a5d69eb49618e8052308b8a944208ceff3d60966271`  
		Last Modified: Tue, 03 Jun 2025 23:01:05 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7366b53130a2c770022a6ffa36820819e2b0db79190377b50d41ce720410ac`  
		Last Modified: Tue, 03 Jun 2025 23:01:06 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7943d8c4c46514cd47b24180aab20cf3d8c874887cf0a46e620bf1da8d8c0e`  
		Last Modified: Tue, 03 Jun 2025 23:01:06 GMT  
		Size: 5.5 KB (5475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f9a39f9db91b9885530a7f719d822858fc216358523bf6f467a09bb69884a2`  
		Last Modified: Tue, 03 Jun 2025 23:01:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:40f9e369f6ab5fed389ef9426eb26b7eaa8828f35e5c23a41fb73f640a58bf28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fd6f5bebf9c72916c742937298083c53c8f5f14e5b29fdc9b0c076846c4e22`

```dockerfile
```

-	Layers:
	-	`sha256:3fd75b56ed67b88c6424146c2f39b820c2b216168ae24a994d4d20802d47292d`  
		Last Modified: Tue, 03 Jun 2025 23:01:09 GMT  
		Size: 596.7 KB (596749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:785cc277ad19a04eaeb5a7c78ddf94a30bed53c9170ba9c0e75417f65aee432b`  
		Last Modified: Tue, 03 Jun 2025 23:01:09 GMT  
		Size: 43.4 KB (43433 bytes)  
		MIME: application/vnd.in-toto+json
