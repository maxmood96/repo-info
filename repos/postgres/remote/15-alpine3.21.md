## `postgres:15-alpine3.21`

```console
$ docker pull postgres@sha256:c8078062608d5eff0a466d7f20490dcf467fc12ad062be62a8237551bd633131
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

### `postgres:15-alpine3.21` - linux; amd64

```console
$ docker pull postgres@sha256:8c6a5975a20479eec6892368a5682c88a86a42437a475747956c1ba70f6325fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (110954708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e461e4ffb63d03e1ac7e4b3f67b9cbd05beb930cb67e0a6edd223379a6a350`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=15
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=15.14
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7d3f991a761ec3b2eb609de2b9dc00d2108ac7d921da41e095ea7e4a922621`  
		Last Modified: Wed, 01 Oct 2025 00:34:10 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ffda7168ab4027f76a6ad24877314dd4ab112e3e3257bc518cb82a442a2789`  
		Last Modified: Wed, 01 Oct 2025 00:34:10 GMT  
		Size: 915.4 KB (915352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3038d06cf7689a1384c4beb8c22071553a5a4bf216100033c1602e386573133`  
		Last Modified: Wed, 01 Oct 2025 00:34:10 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed152c8fe7367a4b088a9c47572ac8194ec1adb25d1658ada0bcb602acc668bb`  
		Last Modified: Wed, 01 Oct 2025 00:34:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f0de7e5b758fd8307b6fac910b95cc0a8f565085fbf93c808e7036bcf7a845`  
		Last Modified: Wed, 01 Oct 2025 00:34:27 GMT  
		Size: 106.4 MB (106384667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a898662175f033de08cf91964a59fe7376a4cb1cac4cb83ba19e964105fa37b4`  
		Last Modified: Wed, 01 Oct 2025 00:34:11 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749a1197fe2fbde04ac7a1885680ccda604178fbff3fc14464c84b2e8e6972b4`  
		Last Modified: Wed, 01 Oct 2025 00:34:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc968db5b7220333ad1ddf445193e51284286ce5a7217dd9ca0129f8bab76bb6`  
		Last Modified: Wed, 01 Oct 2025 00:34:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323b046dce036de5fc0863a6f65e2567601e33f08a25be07445e9d4848bd779d`  
		Last Modified: Wed, 01 Oct 2025 00:34:11 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40c5682af2cc74a2d57159987d41cf0e20600981e356dfe7b5c56d7b5d8da09`  
		Last Modified: Wed, 01 Oct 2025 00:34:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:d76e725307d5843998653bddc1823cd74c923e9b19e0c0ee1f6bdb896e46249d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.5 KB (642503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75fd4ccee9d377cf9c09f6d25937ecebd50f1aa8615f400fa2211a199b848540`

```dockerfile
```

-	Layers:
	-	`sha256:8b74beb52483b8b62f580388b696025aaf0bbb09c10e3813234e870d102f5887`  
		Last Modified: Wed, 01 Oct 2025 14:14:40 GMT  
		Size: 598.7 KB (598692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61107b080d492f8463bda512ad7200cb3a9dc5a90d439a1dc890b533d6d2dec7`  
		Last Modified: Wed, 01 Oct 2025 14:14:41 GMT  
		Size: 43.8 KB (43811 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.21` - linux; arm variant v6

```console
$ docker pull postgres@sha256:f8d3f3bc5dca3ac04326ddab45b5245aaf82097fb493b0438f3046d48ff3ce51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88289892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644b71393019ffa2d564f91300d688564c17e1bd068843d3e0cc198756844106`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 30 Sep 2025 18:58:13 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=15
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=15.14
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f432460fed417a847f366711fd6a1511b2886effd39191b05aaf5ef6590f0d87`  
		Last Modified: Wed, 08 Oct 2025 22:04:03 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872e21f054224121d06fc6fe3f85c9a32f278d296a742f4724995a17b7e7604a`  
		Last Modified: Wed, 08 Oct 2025 22:04:03 GMT  
		Size: 886.1 KB (886097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4149ede813f5fbd3f08627aaf97f361909afaf3876447a39be94c9cd9054631b`  
		Last Modified: Wed, 08 Oct 2025 22:07:05 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed450ae4fbe4547f26ca20e13a6276a43d235f81c5a2374301cdda3045387595`  
		Last Modified: Wed, 08 Oct 2025 22:07:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33dacb9c605de79405cddd744624fd59ccbad7956d62f10b8021ed56748d831`  
		Last Modified: Wed, 08 Oct 2025 23:10:31 GMT  
		Size: 84.0 MB (84021214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab2e91195c3089bb269ce4315dd9201347f763d21e9bb902f91b44c19e16162`  
		Last Modified: Wed, 08 Oct 2025 22:07:04 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f51b770a0b14952948fd42c3aa14b14e3f43812e0a366ff6ab366e1fd31de5`  
		Last Modified: Wed, 08 Oct 2025 22:07:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda0590c8c7ca04574c5f59e9da80a5eb8313819046f830a2229a2778934db11`  
		Last Modified: Wed, 08 Oct 2025 22:07:04 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e746b48496e26a1aaf3df6107c2402b512ef4e6fcd6b68f6650e296cd72d4f`  
		Last Modified: Wed, 08 Oct 2025 22:07:05 GMT  
		Size: 5.9 KB (5931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcff4e4719970d0a34f089488076028b3c08559b6cf70002207d96c1eb0b03e7`  
		Last Modified: Wed, 08 Oct 2025 22:07:04 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:9de924110ef1764a4b65d420f8a9e8727b4d3d6dfd5e46ab6a84d42d421b7758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 KB (43757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a6831d9393b81f0cb468189bd367efa0708f8a033e279ca4f2c98f93d5e582`

```dockerfile
```

-	Layers:
	-	`sha256:cddd680c3fd6698f754d4ea1fb1d9141e867320400462db252a6ed3b97e7569d`  
		Last Modified: Wed, 08 Oct 2025 23:09:54 GMT  
		Size: 43.8 KB (43757 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.21` - linux; arm variant v7

```console
$ docker pull postgres@sha256:3f124aff2f280fe18fce85c0b0bb18c177ccd04f00714cb4a07af37f57a707ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83523676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b27a5854535ea48c45cac2af53ecf7f882921e7124ae4bd656044264cd33f36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 30 Sep 2025 18:58:13 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=15
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=15.14
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da6d9b300977277d07643fdb6884ed03312e689349c1a7f7014844801152f32`  
		Last Modified: Wed, 08 Oct 2025 22:09:03 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04ef703528cacc6e1efe6fefe59c26de789c97def8418e7fff2013ede5a77f6`  
		Last Modified: Wed, 08 Oct 2025 22:09:03 GMT  
		Size: 886.1 KB (886106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd57fef7aafed681ab33cc53aa449cdd4ed8e2df5e9b4b7e85bc723e0203d031`  
		Last Modified: Wed, 08 Oct 2025 22:09:03 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e91f50b8a0416c3f0a7a8008ed7c4ab6071085f89e4a21c8506a80ad00a858`  
		Last Modified: Wed, 08 Oct 2025 22:09:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe066df64ca6606053aa15b5d36012331a3c189415d2312376a2644b54bedb7`  
		Last Modified: Wed, 08 Oct 2025 22:09:11 GMT  
		Size: 79.5 MB (79521842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0af1e86c8a979089f4e0cfc6cbd5707ba90cdb578e90aba4952c9dbdbbb24e`  
		Last Modified: Wed, 08 Oct 2025 22:09:03 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b2346031f953d86cd3c7a9ad8fdf4e64dc9677156568d77ae5dd5568e33d27`  
		Last Modified: Wed, 08 Oct 2025 22:09:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c71dd8f543bd252a2d8ef16b256e1575b2c9425e383ff9305fcf2f34441d263`  
		Last Modified: Wed, 08 Oct 2025 22:09:05 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f87c0a2f40a626b47f784e8a68dc5bb8996dd5b3544e4bf4ff1cba30c37c3c`  
		Last Modified: Wed, 08 Oct 2025 22:09:04 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7916e5b4ccb92c055da4378d4cde11ad00e9202aa6129eed6454bdac7493873`  
		Last Modified: Wed, 08 Oct 2025 22:09:04 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:372bf27b2897b63818d2ae8891cf0118cb85e9b4271f73c4ad160b71525fda98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.7 KB (642685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517a2342b497b2ebf1fb888f3c5a2cc63c1d406f618ada58ca1454aec05cec10`

```dockerfile
```

-	Layers:
	-	`sha256:6f55f0193827c0b58c0a667c530e27829485f2c29f70de5d73824f2855830202`  
		Last Modified: Wed, 08 Oct 2025 23:09:57 GMT  
		Size: 598.7 KB (598712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:650e569adece128042a1eb262399b2f53fe84221e8070562579fd1437261d854`  
		Last Modified: Wed, 08 Oct 2025 23:09:58 GMT  
		Size: 44.0 KB (43973 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:96c9962f83158ae2977b23baf3fc800601c7f59389581443ef720bd1c0077cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104585394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f00b6241e15b77d271e28e3bb8c10706016f01cb6f4e3fd4ec8dda21fe4281`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 30 Sep 2025 18:58:13 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=15
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=15.14
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b4c7abde1c3dda997255d410115cc4a8de0f5b1c2cc22cc57d25d9f73b6f94`  
		Last Modified: Wed, 08 Oct 2025 21:45:05 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2716a5bb50754f665b2782deafc5aea5ef6705120c607d5d9f62652a9c215a91`  
		Last Modified: Wed, 08 Oct 2025 21:45:05 GMT  
		Size: 873.5 KB (873456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115ea74514118212a2ceba594e0106f7332a9508673f0ea6479bec1023280cf8`  
		Last Modified: Wed, 08 Oct 2025 21:45:05 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e736e25ef4c772108b7103d16d96d12797202ca834b90782016b07d9b009ad35`  
		Last Modified: Wed, 08 Oct 2025 21:45:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f458a3e3025c38b58fd4f2469d24f8b8c92c4516348a8ba74ec634799d7f87`  
		Last Modified: Wed, 08 Oct 2025 21:45:16 GMT  
		Size: 99.7 MB (99702476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1834f452df50be3e0ce3ec23396bf2ddebeb8caca5173e56b94191e85cab0bde`  
		Last Modified: Wed, 08 Oct 2025 21:45:05 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c388be54ea9c459eeab1b07292b3fd42fe8712c75c0d81aef205064fc7b4c3`  
		Last Modified: Wed, 08 Oct 2025 21:45:05 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2753bf2634a0ddbaaf6da3413b8b66035a60d3aab2ef6e887f9672b925fca7e`  
		Last Modified: Wed, 08 Oct 2025 21:45:05 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f276191639fd93f03662db81d26529100fb6de28de354dd24f5c81b8e8cc8215`  
		Last Modified: Wed, 08 Oct 2025 21:45:06 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee8a0e9f833a0ad2ca25e42f88b4b19a4dd3f65be7535beb1d1873388330cc7`  
		Last Modified: Wed, 08 Oct 2025 21:45:06 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:a0a2cdf0a2c70954ad10a35a38d5105bd13b227eab5132057b3916e0e7f481b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.7 KB (642729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1579a921262cbc1e2da5dd08e1c51ca1a01d2579d8576bf0d8dd97e31bb1253f`

```dockerfile
```

-	Layers:
	-	`sha256:83e2ce5eb07d1e801a137ddab61822d6e11e9944c61158cc3afe4b31d991ddb7`  
		Last Modified: Wed, 08 Oct 2025 23:10:02 GMT  
		Size: 598.7 KB (598724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:962659dfe95a4b4daf6106b5cdafe0c8092bb8fa5db7689f31e42b0341cd285f`  
		Last Modified: Wed, 08 Oct 2025 23:10:03 GMT  
		Size: 44.0 KB (44005 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.21` - linux; 386

```console
$ docker pull postgres@sha256:1c7b14912368117e033f4a7eb7516e5a367168cdb8c2c25904ba4d0eb6af0adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114826004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc148533bf9bc14ee55c7e354596ddbad9fe43c315200572d5494b496bd5f20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 30 Sep 2025 18:58:13 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=15
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=15.14
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef4a9bf41a328de86f85f9d92ec054041774c91843fd689fd89875fe41b4f3e`  
		Last Modified: Wed, 08 Oct 2025 21:39:11 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff4ec9d2598a69c19649c337f8acd9499e92272ece2f4d9e001efa16befef13`  
		Last Modified: Wed, 08 Oct 2025 21:39:11 GMT  
		Size: 890.6 KB (890604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b314a4bf5d82240030ce2b43046c55f2ebfcdfcd9b692e37fd42b55946c5fbb`  
		Last Modified: Wed, 08 Oct 2025 21:39:11 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b89d01fc4355dd874222040f72502742505ba3dc1fa58806e3a93d701a5bc39`  
		Last Modified: Wed, 08 Oct 2025 21:39:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ffa97d27078797a5579a92b52f1da17a402bce25700fbba023087a6c7be836`  
		Last Modified: Wed, 08 Oct 2025 21:39:28 GMT  
		Size: 110.5 MB (110453580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1947c6dac181eeafa18815fb03b5c927a3c0da4b9c53f27ff3c2777fb907e701`  
		Last Modified: Wed, 08 Oct 2025 21:39:11 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693a2371ec6bf75607d3f188001550cc62ac8d47631ed3b17c48aa44f7923a62`  
		Last Modified: Wed, 08 Oct 2025 21:39:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12be5429582aae60ce37f1d5cf1c0b8f2e59483e147933a60f481cb0ebe63d92`  
		Last Modified: Wed, 08 Oct 2025 21:39:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd6fe7b2a714a301981812acc7167901b9f013c5677ea58e81988accd3dbe68`  
		Last Modified: Wed, 08 Oct 2025 21:39:11 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39534e623de2a442c9d2ed0d767c3e0ce116fbf007da23f6163dde71f9067a5`  
		Last Modified: Wed, 08 Oct 2025 21:39:12 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:34cb3d4254d448acc8e5e5e2acf6d8ae513b795bbc3336528be16343b4398be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.5 KB (642450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b40ae16c2d9a546fc623eb24c24068af4a2c2935873ac775ed09d736cb8989d`

```dockerfile
```

-	Layers:
	-	`sha256:2e39e23d6301a7d0d5c728bb93bbf0fcf9812536a5724702419cb615a39cc082`  
		Last Modified: Wed, 08 Oct 2025 23:10:06 GMT  
		Size: 598.7 KB (598677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e9f18f9012ee63d87ca3b90d5f137d28139aff0a9a88d59237925210d380976`  
		Last Modified: Wed, 08 Oct 2025 23:10:07 GMT  
		Size: 43.8 KB (43773 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.21` - linux; ppc64le

```console
$ docker pull postgres@sha256:1bed55789e1205f8690d980264b73f5c5736b299571aaca8a27bf005047f78bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94565238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455375e03a74d8586d6b7724c32a538fec8cad06f005221287a609926735b48b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=15
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=15.14
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747bf6778b8e7ed31d4743686f1f50485c5c074620417743c59a087cdb5f9186`  
		Last Modified: Wed, 01 Oct 2025 08:36:58 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ded0eec492104ecd2eae20f50bf37ad15ee8c2428edc86b79a41ad80e9addb`  
		Last Modified: Wed, 01 Oct 2025 08:36:58 GMT  
		Size: 873.8 KB (873763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcbb7374b33366d8cc37a51cf30a09f597c947f160ec3c072a6c438ddf6707d`  
		Last Modified: Wed, 01 Oct 2025 08:59:08 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe80ba2325ccbca20c2bc91de1403de3d608e89a78544898eba2cf99687aca8`  
		Last Modified: Wed, 01 Oct 2025 08:59:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0913945f076a582cdc0ce09c5a1fb70ae6de326f0604d57bd4649cfd3857b54e`  
		Last Modified: Wed, 01 Oct 2025 09:01:11 GMT  
		Size: 90.1 MB (90105225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9242a6a61666f59de453f9b34fabaa33f044c6cecece62693a070b26c9bc9e`  
		Last Modified: Wed, 01 Oct 2025 09:01:00 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea26910e15fb19df69d9e7075defb1c3587ab62a39248a3a47a3940eec007af`  
		Last Modified: Wed, 01 Oct 2025 09:01:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2fa75113ae06813af22cf089273e28e0de501004bd75bc43555e91b4e4544f`  
		Last Modified: Wed, 01 Oct 2025 09:01:00 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1d19799e62fe6f7e6bf84704057683d2cc6f5a98e2ecb5413b0672ba5b1f4b`  
		Last Modified: Wed, 01 Oct 2025 09:01:01 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a69edb93f9587c1e702600c70e2bf5af7302bbbb11c52f9592dad04a56fa99`  
		Last Modified: Wed, 01 Oct 2025 09:01:01 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:b759a7c300fac5436d35bc11cb0ea9e65109e5858ed81c402997d4538fb4145e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.0 KB (638954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6978e742bd75049e8c16ec1bf11b25fefe3aff7097f1418a8fe16e6ce4d20b53`

```dockerfile
```

-	Layers:
	-	`sha256:fe2add037231b3957432d5362570c65a588fe935d78ff066933b81a9e7bede0d`  
		Last Modified: Wed, 01 Oct 2025 20:12:30 GMT  
		Size: 595.1 KB (595101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:792080cc121b266e0902c757c4636f2265e2620840406f29950fc739fefbfbcb`  
		Last Modified: Wed, 01 Oct 2025 20:12:31 GMT  
		Size: 43.9 KB (43853 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.21` - linux; riscv64

```console
$ docker pull postgres@sha256:f632a1d3d95b0762927ffd44bca2ea0705ef0328569411ee995e3bb9b166b23b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110554912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794555d99acfe1c5d3a3f9f6e7b16c45c0b8446c500b76afe13143684030c435`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=15
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=15.14
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f442f14b9fc184be7b5b23f9b5362306d14b41b75f0fc847fcc5851ab3402e5`  
		Last Modified: Wed, 24 Sep 2025 00:47:22 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a806fe08f5cb13a300574c46c89d7d784c57ea301fece231af5a28695589eac`  
		Last Modified: Wed, 24 Sep 2025 00:47:23 GMT  
		Size: 860.8 KB (860848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447da1560e7579310046d88af470ba2bfe8a6d5d8e228e2068d32f9409c44707`  
		Last Modified: Wed, 24 Sep 2025 08:50:53 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19719383b23bb55e69b9acb371535c6a6bcae9dcbb54cebd17541e6b8e59b49`  
		Last Modified: Wed, 24 Sep 2025 08:50:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171a4fbc0e6be6f576fb06e816234f4af2a5c88372a6d896140e0337c5f9200b`  
		Last Modified: Thu, 02 Oct 2025 20:29:12 GMT  
		Size: 106.3 MB (106327846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e1d9a48c177786c2a45c4bbd0e961d9ed6fd94d33ce8100d2c9cf6acd7eb5`  
		Last Modified: Thu, 02 Oct 2025 20:28:58 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7b13c516f12b3ad13e39262da60a8774e0d852e6fa2b4516064ac1f6f89884`  
		Last Modified: Thu, 02 Oct 2025 20:28:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3082cf864aebd755c20eebc8c5fde6833df0319e7e1e396707828c443cfbcc2b`  
		Last Modified: Thu, 02 Oct 2025 20:28:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d86ce362c5a67a8fad34bed26233dfb4915b1d5267ffe7812e6a0c0513638c`  
		Last Modified: Thu, 02 Oct 2025 20:28:58 GMT  
		Size: 5.9 KB (5931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ebf2be2e4c982657017cb49e55153c6b9e567a1c81de57b1044630cbfbc2e5`  
		Last Modified: Thu, 02 Oct 2025 20:28:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:f21a9a638daeb5f1f036f48ac48be1998dbb093317624ccd161262891db529ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.6 KB (640618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd6f5e749221f1a9659fea4a567780d3b0302eaf7be15c881ef61375f2cf5e6`

```dockerfile
```

-	Layers:
	-	`sha256:ad0d76efdf3f60d905e2b7cd4312e0a6b2e3d1e613bad56e8c019aa313522d81`  
		Last Modified: Thu, 02 Oct 2025 23:08:22 GMT  
		Size: 596.8 KB (596759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c682b5e062491bf3160a36eb2aaa917f20fa78ece9696971452672152d6d75e`  
		Last Modified: Thu, 02 Oct 2025 23:08:23 GMT  
		Size: 43.9 KB (43859 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.21` - linux; s390x

```console
$ docker pull postgres@sha256:3e92935297d8e5fca851743d65c8c5c1d5e27ddb27a2dd25cd62c6bf408faeb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119307994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580af93a37729ef9fc63cbb54a364570043d283f42d420e2b98373557e23bfb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=15
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=15.14
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3a0b3e42a00821c504172afe5ad33497b04821fb945d8f1762c22b804de062`  
		Last Modified: Tue, 23 Sep 2025 22:00:10 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfde9cde752b53d44f7ef28a4eaabe5d98c6054f6df4adb3d525fe6d7846494`  
		Last Modified: Wed, 01 Oct 2025 04:51:03 GMT  
		Size: 891.2 KB (891242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4fc88dd289be74ba2ca2ead2356391f5695518a0bc2bbbc86b46e2db34fe01`  
		Last Modified: Wed, 01 Oct 2025 05:08:04 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b672fc6af4622dc19a1e29bc041de271a18f9da1c4f630ee343bbf6d54a0301`  
		Last Modified: Wed, 01 Oct 2025 05:08:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0336b5b218ba4bbec3094738e10694a8b3489ef962124aa1d0b6353f29edf84e`  
		Last Modified: Wed, 01 Oct 2025 05:15:34 GMT  
		Size: 114.9 MB (114937531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc8feed26979931e111886c78fd9ef16688b17fbb735c3d4b8f8f95a107863d`  
		Last Modified: Wed, 01 Oct 2025 05:15:23 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a01ebdf87e64ddae6c8ed23edac87e510a1d8e4660c34bad1e43de4e4da2c3`  
		Last Modified: Wed, 01 Oct 2025 05:15:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a35a74b053038e448aaf4c4f3b3d9b8c9e3e6af0834fd33fd5596a47bea2aab`  
		Last Modified: Wed, 01 Oct 2025 05:15:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c069641d7c8f5b2083df189966cc12ae42c61822c97f957c79e937fe8964e35`  
		Last Modified: Wed, 01 Oct 2025 05:15:24 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbf65b495c64ad9929a0c6ad3fd1d0ec81c1348ef3c1ac7f706911b96e839c5`  
		Last Modified: Wed, 01 Oct 2025 05:15:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:91155a553d487a987aeeb3f9f3ceb6bdbee149f27dcf9dd8deb1adc527bbbae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.6 KB (640552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3e3d86f4249260cc2836b22fd1f59ba756b73ccafd77af53cd3b24b5fc6e03`

```dockerfile
```

-	Layers:
	-	`sha256:b3c9b178e954fb137c27233e05de5856d69923692cdc962d33a2a32d1bc4fe4a`  
		Last Modified: Wed, 01 Oct 2025 20:13:15 GMT  
		Size: 596.7 KB (596741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517d263918eb6a3bdd5e689cfdd92d9e78bfad97377ce2e4306c03e17b19841f`  
		Last Modified: Wed, 01 Oct 2025 20:13:15 GMT  
		Size: 43.8 KB (43811 bytes)  
		MIME: application/vnd.in-toto+json
