## `postgres:18-alpine3.23`

```console
$ docker pull postgres@sha256:eca6fb2d91fda290eb8cfb8ba53dd0dcbf3508a08011e30adb039ea7c8e1e9f2
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

### `postgres:18-alpine3.23` - linux; amd64

```console
$ docker pull postgres@sha256:7c79e2ccf92fe341e26d9df68c3cc8e8d1999728f1d0290fc9cc58158d327acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.0 MB (111951277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d29e8dfc4434d20bde10afa801af7eb4a0e4d597cf240da6a4e7d262bcd067f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:23:07 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 04 Dec 2025 22:23:10 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 22:23:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 22:23:10 GMT
ENV LANG=en_US.utf8
# Thu, 04 Dec 2025 22:23:10 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Dec 2025 22:23:10 GMT
ENV PG_MAJOR=18
# Thu, 04 Dec 2025 22:23:10 GMT
ENV PG_VERSION=18.1
# Thu, 04 Dec 2025 22:23:10 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 04 Dec 2025 22:23:10 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 04 Dec 2025 22:25:38 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 04 Dec 2025 22:25:38 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Dec 2025 22:25:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 04 Dec 2025 22:25:38 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 04 Dec 2025 22:25:38 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 04 Dec 2025 22:25:38 GMT
VOLUME [/var/lib/postgresql]
# Thu, 04 Dec 2025 22:25:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:25:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Dec 2025 22:25:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:25:38 GMT
STOPSIGNAL SIGINT
# Thu, 04 Dec 2025 22:25:38 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Dec 2025 22:25:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4005b2bbd055373da09b338b3be7de4b843676d8e9cf05983bfac712a8d4de43`  
		Last Modified: Thu, 04 Dec 2025 22:26:02 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9048358bf495638a06aca0eeb47ab47d2c08ac1cb5ebe021c069d464221f24f8`  
		Last Modified: Thu, 04 Dec 2025 22:26:02 GMT  
		Size: 922.9 KB (922932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b0aab6fe875d4a13b3a48ce6616ee989c94e274b43208fbe86ac5b7c664fa7`  
		Last Modified: Thu, 04 Dec 2025 22:26:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edd81474bccfea144471e1e1ec1671f7e790027c2c3a6419f4adb6fd0603a77`  
		Last Modified: Thu, 04 Dec 2025 22:26:19 GMT  
		Size: 107.1 MB (107142841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5756c37098a3a8cf26b0b4830d8ec14d5a0d20ccc2452ad07897bd58b16765`  
		Last Modified: Thu, 04 Dec 2025 22:26:02 GMT  
		Size: 18.8 KB (18772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64140eb696362b9fb4a7291b9ca6b1b1ffb727ae4056fd5124c1d27b61b7d0f2`  
		Last Modified: Thu, 04 Dec 2025 22:26:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f798bec5cdac65d9f8dc5a2ffe2915378ceadd94f968e240f1d5e2ee191c5038`  
		Last Modified: Thu, 04 Dec 2025 22:26:02 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d8dff923796e1d9dab440195504b26d9ff59b04e0966dfcf890716b714d06b`  
		Last Modified: Thu, 04 Dec 2025 22:26:02 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b508cd02184169164dfcbe8beda660e7d55af2a1cb00a0d9d34a258dbc4262`  
		Last Modified: Thu, 04 Dec 2025 22:26:02 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:5380109c7fdabcf373b311c4a62f8289fd98d8deeee56693f93b853b37fa3ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.4 KB (643424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012f3016e066f7373481b7771b1b14e78293ad641b85ed44cef36a3dc3964b20`

```dockerfile
```

-	Layers:
	-	`sha256:d03c6aa82107c94b2cf06dc2ce9275a9f75b01e078d8ec9432feb8bdc01a1e3f`  
		Last Modified: Fri, 05 Dec 2025 00:10:57 GMT  
		Size: 600.3 KB (600312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:023d3ba76e75bf3c01c93e217ee0522e16a22d6c92bb695bbf0cab375bf02867`  
		Last Modified: Fri, 05 Dec 2025 00:10:58 GMT  
		Size: 43.1 KB (43112 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.23` - linux; arm variant v6

```console
$ docker pull postgres@sha256:0548c3f9f5fa9cda741874c467154079e69c84a13ba5b7c2c0f67f31d3b720d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91420817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8033eda0eb70afe83c4f4e9b315097811fd9d4bda3c2c71ad5bc8e3318ab6c17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:23:09 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 04 Dec 2025 22:23:12 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 22:23:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 22:23:12 GMT
ENV LANG=en_US.utf8
# Thu, 04 Dec 2025 22:23:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Dec 2025 22:23:12 GMT
ENV PG_MAJOR=18
# Thu, 04 Dec 2025 22:23:12 GMT
ENV PG_VERSION=18.1
# Thu, 04 Dec 2025 22:23:12 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 04 Dec 2025 22:23:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 04 Dec 2025 22:26:01 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 04 Dec 2025 22:26:01 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Dec 2025 22:26:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 04 Dec 2025 22:26:01 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 04 Dec 2025 22:26:01 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 04 Dec 2025 22:26:01 GMT
VOLUME [/var/lib/postgresql]
# Thu, 04 Dec 2025 22:26:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:26:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Dec 2025 22:26:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:26:01 GMT
STOPSIGNAL SIGINT
# Thu, 04 Dec 2025 22:26:01 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Dec 2025 22:26:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a164fe31a0647e8a9253b2d62e0afe6067507dcf069238382699da1fd660e78c`  
		Last Modified: Thu, 04 Dec 2025 22:26:18 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a7e23fa3e88a222ebe54cb2047c8a826a80273731b7c5acb9d46fb526ea5ac`  
		Last Modified: Thu, 04 Dec 2025 22:26:18 GMT  
		Size: 889.5 KB (889468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e29d0014d8537c15b91092c937a30dfee4f23c30a7a7e7cd35b19bbadf64740`  
		Last Modified: Thu, 04 Dec 2025 22:25:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da663131cffcedc3637713a1b90cb8c078713dddd6e31b96efa1203d1cf7ed0`  
		Last Modified: Thu, 04 Dec 2025 22:26:26 GMT  
		Size: 86.9 MB (86937260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d90852917ab1ac125eb51b0b48dc72c5ce39757a2c63df3c9d2965398c45228`  
		Last Modified: Thu, 04 Dec 2025 22:26:18 GMT  
		Size: 18.8 KB (18775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c126bdd32fb2846e70a55fc3a90a713e28b3021f496f0e5a5a54b720c013515a`  
		Last Modified: Thu, 04 Dec 2025 22:26:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9d69d6e784583c5c2f9007f7630bbabf5db2aa946ed9601ff3268723ba27e8`  
		Last Modified: Thu, 04 Dec 2025 22:26:18 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba47329b203ada5f63bfe9ff8a7119c2bb3622d66afbac37129f8756dcc3c3be`  
		Last Modified: Thu, 04 Dec 2025 22:26:18 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930ab5db22e264ca08ed27f9da7dc9a57b7b22b42d03aa267d663703f0ac8dab`  
		Last Modified: Thu, 04 Dec 2025 22:26:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:a3f13321218ddadc392eed13bbb96d8a5a97c6682bb2242de6ed73a0379f39f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 KB (43078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ea6c20a1bce16726f41d2f97290a401e7a8388f17ee61035187cf852d4fe3a`

```dockerfile
```

-	Layers:
	-	`sha256:a55ee6aec30d64603bf6cc45c26b1171d3ce9d6d980b3b49a9e63958e05b4abb`  
		Last Modified: Fri, 05 Dec 2025 00:11:01 GMT  
		Size: 43.1 KB (43078 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.23` - linux; arm variant v7

```console
$ docker pull postgres@sha256:37d87f8cb57875dc14879430393883296d3e0180d0f3ccb62cc69cc6e3825132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86570540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6aa356933a66b16bfd9dcb7c6c9e5506d1d41fadf42b98739c7164dacb3c137`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:20:25 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 04 Dec 2025 22:20:28 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 22:20:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 22:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 04 Dec 2025 22:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Dec 2025 22:20:28 GMT
ENV PG_MAJOR=18
# Thu, 04 Dec 2025 22:20:28 GMT
ENV PG_VERSION=18.1
# Thu, 04 Dec 2025 22:20:28 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 04 Dec 2025 22:20:28 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 04 Dec 2025 22:23:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 04 Dec 2025 22:23:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Dec 2025 22:23:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 04 Dec 2025 22:23:17 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 04 Dec 2025 22:23:17 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 04 Dec 2025 22:23:17 GMT
VOLUME [/var/lib/postgresql]
# Thu, 04 Dec 2025 22:23:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:23:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Dec 2025 22:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:23:18 GMT
STOPSIGNAL SIGINT
# Thu, 04 Dec 2025 22:23:18 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Dec 2025 22:23:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f390c8e62ac2d1194796b54c1967c2afbc60b505ac546b4d5659c77a3c8fd9`  
		Last Modified: Thu, 04 Dec 2025 22:23:37 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af2f96b6f8222e0e4462046fca9db26815afa3dd91a9eb8a1feeadd07a85ab7`  
		Last Modified: Thu, 04 Dec 2025 22:23:37 GMT  
		Size: 889.5 KB (889478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afef7380777c6cb1277b9c1099903291e97389467b2750611c46d85b7f0d100`  
		Last Modified: Thu, 04 Dec 2025 22:23:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bf0c0adccc495d0fd119e4476634fc3802f059dd7a8e6ff013444e0a0d2a99`  
		Last Modified: Thu, 04 Dec 2025 22:23:43 GMT  
		Size: 82.4 MB (82376402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ebc641b085c09f247e454f2b5042acfea8f761f21f854260e457c69b97edda`  
		Last Modified: Thu, 04 Dec 2025 22:23:37 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6daa39278057c4e4dce59ff75191305c94fec6f42840430515ef9de71567dbb1`  
		Last Modified: Thu, 04 Dec 2025 22:23:37 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c546534f3e4a2daf8d074d23f78d56fbdf6434c889ac097a938a8ac15e2f33a7`  
		Last Modified: Thu, 04 Dec 2025 22:23:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba964f9790e571c96e0863cfce094f26e164c76f263ab3628795b22fd9ed947`  
		Last Modified: Thu, 04 Dec 2025 22:23:37 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41197bab7a9689f7bfcadc66a4ceece1c182e9ea5603767b4253c31b0ebd92d5`  
		Last Modified: Thu, 04 Dec 2025 22:23:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:34b0068d3524314c40a837c04362ba93a21637057fe529115d82db53466dc3c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.0 KB (643005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9196d019614c5a73a9c46553d7811901679b6d80203d997beff5264da0a57715`

```dockerfile
```

-	Layers:
	-	`sha256:26315847696959c15c0446343da9fa1825dbd462a6ab8a57423c41f4c5fe2519`  
		Last Modified: Fri, 05 Dec 2025 00:11:04 GMT  
		Size: 599.7 KB (599714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4a0d9790d84028c8921f5afaa726a177f192d2cb91ef722a089367dbc1d73a`  
		Last Modified: Fri, 05 Dec 2025 00:11:05 GMT  
		Size: 43.3 KB (43291 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:19d41e875195174af5fecc14e14be36c0ecf0789599edce6d9a30a7e737c3032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110131387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2977230bd98b50ecd4ea5007b206eeaaa0d5b5005100cb4df142e9f7864f86d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:21:53 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 04 Dec 2025 22:21:56 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 22:21:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 22:21:56 GMT
ENV LANG=en_US.utf8
# Thu, 04 Dec 2025 22:21:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Dec 2025 22:21:56 GMT
ENV PG_MAJOR=18
# Thu, 04 Dec 2025 22:21:56 GMT
ENV PG_VERSION=18.1
# Thu, 04 Dec 2025 22:21:56 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 04 Dec 2025 22:21:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 04 Dec 2025 22:24:22 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 04 Dec 2025 22:24:22 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Dec 2025 22:24:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 04 Dec 2025 22:24:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 04 Dec 2025 22:24:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 04 Dec 2025 22:24:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 04 Dec 2025 22:24:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:24:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Dec 2025 22:24:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:24:23 GMT
STOPSIGNAL SIGINT
# Thu, 04 Dec 2025 22:24:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Dec 2025 22:24:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492c8880cb7c475d6d9c377c0137c3e69904122a4701e3c67d1fb2220b243512`  
		Last Modified: Thu, 04 Dec 2025 22:24:46 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73dd0d6e2a6c1de94d2e202a7d76a82fe945879a25b1b797d5bfb360a9ee54ca`  
		Last Modified: Thu, 04 Dec 2025 22:24:46 GMT  
		Size: 876.5 KB (876488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72a6c4afc3b9bdfe8916ede8f5b47ddde233db21ed26abcc775bfee4aa4f225`  
		Last Modified: Thu, 04 Dec 2025 22:24:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290229ea38440042754e413e54c464890421d8ecd9b9670f56bf17fb238eb3a0`  
		Last Modified: Thu, 04 Dec 2025 22:25:06 GMT  
		Size: 105.0 MB (105033515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae04ae7488ab9dc5b6571d100e1cb907e3fdc4b7e2dd57b1bf5eeb9e8246997`  
		Last Modified: Thu, 04 Dec 2025 22:24:46 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98436007eba1afee0cde2b937c4a3412f2c7a9ef25b85ecdc7255464d5a62617`  
		Last Modified: Thu, 04 Dec 2025 22:24:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72e3f5a2ab2a71660c3210c220a07febfc11e57317d2e6f494f0f71af1831a9`  
		Last Modified: Thu, 04 Dec 2025 22:24:46 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e622f1a0161cd9bc1d6b00163f4b2917bccf580e2d583b8ca17adee461c96b48`  
		Last Modified: Thu, 04 Dec 2025 22:24:46 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c285079a92066cf4d15c84174b6aca001098e2e7c08da067ae2a3a8d21acb6dc`  
		Last Modified: Thu, 04 Dec 2025 22:24:46 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:4935506dc582953255950891b019de34d6740992932067deadc09f54254aee87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.1 KB (643086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b66917c53bff6dea58f849de86723fe8c65326fb057964103ad8fbe603d5948`

```dockerfile
```

-	Layers:
	-	`sha256:1da183b52fe2dbef9d0899b1868657dd505e3586cf7cd6d28ed2342cca2908bc`  
		Last Modified: Fri, 05 Dec 2025 00:11:08 GMT  
		Size: 599.7 KB (599742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9c5b2c1d59307b211c4d0082f283d44b093d562d7993a1a8ba113e8b01677e`  
		Last Modified: Fri, 05 Dec 2025 00:11:09 GMT  
		Size: 43.3 KB (43344 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.23` - linux; 386

```console
$ docker pull postgres@sha256:1c1cfbabf06fd06656d863a6e5e1a1c00639db406a0b2932909ebfc684a9f939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118113538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d9af7234105ee92a72d55f125fdbeed100ba0537d6018e6d473069e9325a47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:21:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 04 Dec 2025 22:21:11 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 22:21:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 22:21:11 GMT
ENV LANG=en_US.utf8
# Thu, 04 Dec 2025 22:21:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Dec 2025 22:21:11 GMT
ENV PG_MAJOR=18
# Thu, 04 Dec 2025 22:21:11 GMT
ENV PG_VERSION=18.1
# Thu, 04 Dec 2025 22:21:11 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 04 Dec 2025 22:21:11 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 04 Dec 2025 22:23:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 04 Dec 2025 22:23:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Dec 2025 22:23:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 04 Dec 2025 22:23:39 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 04 Dec 2025 22:23:39 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 04 Dec 2025 22:23:39 GMT
VOLUME [/var/lib/postgresql]
# Thu, 04 Dec 2025 22:23:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:23:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Dec 2025 22:23:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:23:39 GMT
STOPSIGNAL SIGINT
# Thu, 04 Dec 2025 22:23:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Dec 2025 22:23:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17caa16467d932a7fea853d6348ede6b96acb2c4e4686258d6518230f33d73c`  
		Last Modified: Thu, 04 Dec 2025 22:24:01 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab2026f28792419b518b825451c23a91b61c08b936a2b36436399c26a1cba47`  
		Last Modified: Thu, 04 Dec 2025 22:24:01 GMT  
		Size: 893.2 KB (893248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d986d0df81eae45bedbaa9d514b3a144e565611bead6be0f3aeeacb85965a6`  
		Last Modified: Thu, 04 Dec 2025 22:24:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1106fe04eba7274f5491d7f36f21240e0930c785636422ce1a65e540a8858e83`  
		Last Modified: Thu, 04 Dec 2025 22:24:25 GMT  
		Size: 113.5 MB (113508237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f0566987e5ba1ca1d144081ffe6fc638d53bd4316aa4410ca987b8f038e6fa`  
		Last Modified: Thu, 04 Dec 2025 22:24:13 GMT  
		Size: 18.8 KB (18776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581e90de429881bc845b62aeddc063ce97b01c784840646b4f40bca226ce05f1`  
		Last Modified: Thu, 04 Dec 2025 22:24:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e93d3797f864817f2f28ccc41f05d1aa53f875b2c5ce4d9b19e9ea066b35577`  
		Last Modified: Thu, 04 Dec 2025 22:24:01 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0dfb64cdfed38f9fc1ec56210ad543661f7b5e1d3c97f5af5816898e3080998`  
		Last Modified: Thu, 04 Dec 2025 22:24:02 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5925e02918c933f7198120d19cb40b2aff7f0355dfc0198295dd639545837aea`  
		Last Modified: Thu, 04 Dec 2025 22:24:01 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:44c90ba49e686128ff92e7b6e97939600b1c2bf9ab4eca4efa66eb190ce828d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.3 KB (643333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f74a030dc2d28d3eac8c8d961ea286f78e566f24b14c824c46aeae860ed3bfd`

```dockerfile
```

-	Layers:
	-	`sha256:30eb0c5f4475c0f8784511866ac8f5fbbc744e78e712c18a47394202ab6df654`  
		Last Modified: Fri, 05 Dec 2025 00:11:17 GMT  
		Size: 600.3 KB (600277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30a154351e1612f375ca526b80aaeb787f5bd354de878db5bd2e9f28c96e285b`  
		Last Modified: Fri, 05 Dec 2025 00:11:17 GMT  
		Size: 43.1 KB (43056 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.23` - linux; ppc64le

```console
$ docker pull postgres@sha256:0c88a30e0744355778e6f8c09929b324ca7c496ea40e72f80b31a7c1ea7ebf3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97050447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe86cf59e136c882f8fbaeb72423dde4f1055967c68d671d3756be5805441d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:19:51 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 04 Dec 2025 22:19:55 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 22:19:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 22:19:55 GMT
ENV LANG=en_US.utf8
# Thu, 04 Dec 2025 22:19:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Dec 2025 22:19:56 GMT
ENV PG_MAJOR=18
# Thu, 04 Dec 2025 22:19:56 GMT
ENV PG_VERSION=18.1
# Thu, 04 Dec 2025 22:19:56 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 04 Dec 2025 22:19:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 04 Dec 2025 22:22:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 04 Dec 2025 22:22:47 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Dec 2025 22:22:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 04 Dec 2025 22:22:48 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 04 Dec 2025 22:22:48 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 04 Dec 2025 22:22:48 GMT
VOLUME [/var/lib/postgresql]
# Thu, 04 Dec 2025 22:22:49 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:22:49 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Dec 2025 22:22:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:22:49 GMT
STOPSIGNAL SIGINT
# Thu, 04 Dec 2025 22:22:49 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Dec 2025 22:22:49 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4059a2642ea065ae9757b9cd6c221d9b0d807a288fbb5b3b03be28c3b5aa9d`  
		Last Modified: Thu, 04 Dec 2025 22:23:28 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d41ce6ede149d659ddaa70993ce94ba64657c097825ad22629ef91006c39d3`  
		Last Modified: Thu, 04 Dec 2025 22:23:28 GMT  
		Size: 881.5 KB (881510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e73b156b196dbd7a32f639eac84e0e9342c84e31dd7f06e2e2176793056066`  
		Last Modified: Thu, 04 Dec 2025 22:23:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e89f9f842dcefecd3ad94e04c491b4f78c63bfd4f4855b028aabd58bd94583`  
		Last Modified: Thu, 04 Dec 2025 22:23:39 GMT  
		Size: 92.3 MB (92315715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21866fc949232946a8a3b8e81a55458f1172209e90c35a46fef78b211698f0b`  
		Last Modified: Thu, 04 Dec 2025 22:23:28 GMT  
		Size: 18.8 KB (18781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d3a541b18f4c31d0508b6f95a93b93d77eb28110e2ccb3cf1b3a036e4a0b38`  
		Last Modified: Thu, 04 Dec 2025 22:23:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9a691a4c15621491fe0f02f35ce2fd316b1ad524c654300f9ee1d3872bdb5c`  
		Last Modified: Thu, 04 Dec 2025 22:23:28 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bffa98955cde7ae2a5c8c79a5ec7e0f30821d98332618baf00edb0e25c31228`  
		Last Modified: Thu, 04 Dec 2025 22:23:28 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1671d012ee7ca6a021c56228d8034f447ac201680af4a8166f13d0422ecb1ac0`  
		Last Modified: Thu, 04 Dec 2025 22:23:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:a36ae52a466c605b29fbdbb81bf3ee904f3cd5210057b798813f9bfd642321b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.2 KB (641220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7a24e54c8ba895753aa54b80ad6c32959024f133a70397fa5a613d86f2a349`

```dockerfile
```

-	Layers:
	-	`sha256:1703356feead158223adbc0f31336def871dd60e26f1358206c1e8bcc2341a4a`  
		Last Modified: Fri, 05 Dec 2025 00:11:21 GMT  
		Size: 598.0 KB (598045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba54ec2c9511548f508f91cc9f98a8920fcc7436820e31f3376a4f53b0325ca4`  
		Last Modified: Fri, 05 Dec 2025 00:11:22 GMT  
		Size: 43.2 KB (43175 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.23` - linux; riscv64

```console
$ docker pull postgres@sha256:b161590ae5164fdb2395b489cb4e1c6271b1f969fc4758229bdfea8453d48823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113208465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6837b553b6163bfc21696b820f51339ac88003f16f01b1b35d3d1f869f5604`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Fri, 05 Dec 2025 02:43:01 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Dec 2025 02:43:13 GMT
ENV GOSU_VERSION=1.19
# Fri, 05 Dec 2025 02:43:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Dec 2025 02:43:13 GMT
ENV LANG=en_US.utf8
# Fri, 05 Dec 2025 02:43:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Dec 2025 02:43:13 GMT
ENV PG_MAJOR=18
# Fri, 05 Dec 2025 02:43:13 GMT
ENV PG_VERSION=18.1
# Fri, 05 Dec 2025 02:43:13 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Fri, 05 Dec 2025 02:43:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 05 Dec 2025 03:33:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 05 Dec 2025 03:33:29 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Dec 2025 03:33:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Dec 2025 03:33:29 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Dec 2025 03:33:30 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Dec 2025 03:33:30 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Dec 2025 03:33:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Dec 2025 03:33:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Dec 2025 03:33:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Dec 2025 03:33:30 GMT
STOPSIGNAL SIGINT
# Fri, 05 Dec 2025 03:33:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Dec 2025 03:33:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291664bb8b7dce2743daba44876e9622d0c6ab2de65fb226fa5a2e612de439e5`  
		Last Modified: Fri, 05 Dec 2025 03:36:44 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d15cb3651c4771f5468271552714d25e62e20e17b4276e4586757bf9431562`  
		Last Modified: Fri, 05 Dec 2025 03:36:44 GMT  
		Size: 868.9 KB (868912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b656cd4e47bea689f9d5174215f9b5aa54f994b325fe9b1ded4f4681308c2842`  
		Last Modified: Fri, 05 Dec 2025 03:36:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c16cd74db6a16f8f51afcf7737c2d0413a93f3d1c889d5d571fbb58a3ce522`  
		Last Modified: Fri, 05 Dec 2025 03:36:51 GMT  
		Size: 108.7 MB (108729824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfb4406c76f126e0ad1c4adf6eb966411e4e762b017e4e9179ad182acc2b149`  
		Last Modified: Fri, 05 Dec 2025 03:36:44 GMT  
		Size: 18.8 KB (18783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef370f256607a9f854c9c3b56111eb9f5b596c02cbf6c474f93f9ab9e507d40`  
		Last Modified: Fri, 05 Dec 2025 03:36:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5030d85c57e368a75bbf31aca88fc4b06d9fd4b25677460fd92c0e6035a56d84`  
		Last Modified: Fri, 05 Dec 2025 03:36:44 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c503693f2908a72df761dc5af0e2ae528066dedd1d211f44116c649338426fe`  
		Last Modified: Fri, 05 Dec 2025 03:36:44 GMT  
		Size: 5.8 KB (5844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053905f16108d243c0eb83f3d57407cdfc2e9d9f58aa5dde3852b5377c3a002f`  
		Last Modified: Fri, 05 Dec 2025 03:36:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:bcf4b417c44114f7b50c1eb1e6b65ec1dfc55dd07cca45bb3f47e1dbd22878a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.9 KB (642885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad79922834641474aa5aa9ed4704e35bf27e6afd4fc137ca90412735c679bbc0`

```dockerfile
```

-	Layers:
	-	`sha256:7b0936c23b71a19587b47d467b9ea1b5452f71c36240c2b3a8c33e58013e910e`  
		Last Modified: Fri, 05 Dec 2025 06:08:47 GMT  
		Size: 599.7 KB (599703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d0fd6ce5ef299bdf9df7a37cf5a7c158e097a84b5d94855e6aeacd626fc7f4`  
		Last Modified: Fri, 05 Dec 2025 06:08:48 GMT  
		Size: 43.2 KB (43182 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.23` - linux; s390x

```console
$ docker pull postgres@sha256:530909b747e19176fbc94609a236dfe1adaf1927178618a48f3af254b70078be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120176583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e53350c5a29fdb7520a72b5e863c07b1eb06ed3430ca6615b5d604ce181d0a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 23:32:11 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 04 Dec 2025 23:32:15 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 23:32:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 23:32:15 GMT
ENV LANG=en_US.utf8
# Thu, 04 Dec 2025 23:32:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Dec 2025 23:32:15 GMT
ENV PG_MAJOR=18
# Thu, 04 Dec 2025 23:32:15 GMT
ENV PG_VERSION=18.1
# Thu, 04 Dec 2025 23:32:15 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 04 Dec 2025 23:32:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 04 Dec 2025 23:38:50 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 04 Dec 2025 23:38:51 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Dec 2025 23:38:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 04 Dec 2025 23:38:52 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 04 Dec 2025 23:38:54 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 04 Dec 2025 23:38:54 GMT
VOLUME [/var/lib/postgresql]
# Thu, 04 Dec 2025 23:38:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 23:38:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Dec 2025 23:38:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 23:38:55 GMT
STOPSIGNAL SIGINT
# Thu, 04 Dec 2025 23:38:55 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Dec 2025 23:38:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31b9e3ed8f234d25da4738dca8de16b285b5a453ad26e857eb6742400fc5080`  
		Last Modified: Thu, 04 Dec 2025 23:39:44 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c834da8b996b863bb6aa0daa48ea611323d5cecc5362f9d668703a853b581d6`  
		Last Modified: Thu, 04 Dec 2025 23:39:44 GMT  
		Size: 897.4 KB (897395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e162dc8f257d6e8e3f50a57fdff16bc516ae12244010353adbe255b09380c863`  
		Last Modified: Thu, 04 Dec 2025 23:38:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0fd01e57e8f538baa6728ede802bd77bdb90661d71483c313959c2fb7710b5`  
		Last Modified: Thu, 04 Dec 2025 23:39:58 GMT  
		Size: 115.5 MB (115529174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ff683b9b19f5eccaee67ed59af4fe5f6e81327b7447b8c1e58b02d267d6cef`  
		Last Modified: Thu, 04 Dec 2025 23:39:44 GMT  
		Size: 18.8 KB (18785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b12dfcd3a101d00f1e6028a1dd8ea6ba19b009c6b42fad22f34bd7214b97149`  
		Last Modified: Thu, 04 Dec 2025 23:39:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65596f15fc3e463de925570f3e2cc5f471e23a266ed48c0f173bdd49b4201684`  
		Last Modified: Thu, 04 Dec 2025 23:39:44 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d36a18c8cd931bb8d69cd7f463b0a1758f725fb7063973582879a55ff28b31`  
		Last Modified: Thu, 04 Dec 2025 23:39:44 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939009ba83e56d2de917451fa13dacafe11b59582f2ca56ba985db515e2dfb86`  
		Last Modified: Thu, 04 Dec 2025 23:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:e2d1e47904d8d96f9b46962bab891e0c3aaeb4e4bc5ea99b67cfca3e81bc7c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.8 KB (642773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78aa34d0aa6378dfa5c142893ef50839c399865a74e822f2b73e70828be368dd`

```dockerfile
```

-	Layers:
	-	`sha256:ae7d16c5fbca92cb5517a01874cb4779d2585a4dd5e1ca4275ad3674e9ba2bf8`  
		Last Modified: Fri, 05 Dec 2025 03:09:29 GMT  
		Size: 599.7 KB (599661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc52b732dcf053d8adde688afc8fcac9c523bdfcd026d4b44a3068b7223174d`  
		Last Modified: Fri, 05 Dec 2025 03:09:30 GMT  
		Size: 43.1 KB (43112 bytes)  
		MIME: application/vnd.in-toto+json
