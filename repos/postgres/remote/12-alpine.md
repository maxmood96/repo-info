## `postgres:12-alpine`

```console
$ docker pull postgres@sha256:b74f3df5c8e168619b7cb2acbca5e85723cc2c684514bc78f86c29d3f7c10daa
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

### `postgres:12-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:21466c789968dd81e25b80cc860e62ee3b1e38434b6401809b8f3d4b334289d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106114797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af259c37b6315eebe973c2819a7003b611b31874e92b75fb365d51119bde2c4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=12
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=12.22
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=8df3c0474782589d3c6f374b5133b1bd14d168086edbc13c6e72e67dd4527a3b
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5afafbeea8a8fd4e2dc0fdcc675a91360c0405d33a26a57bd1a66980134b70`  
		Last Modified: Wed, 08 Jan 2025 06:46:29 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2108423dc6648ad41adf21bf51f9865fcffd16f3a6cd599616cffd99faed17`  
		Last Modified: Tue, 07 Jan 2025 03:19:44 GMT  
		Size: 1.1 MB (1112965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440d6cd4ec7ae1b9843380563a40243e4a9e861513fa31ffb44ddc82bb3139b3`  
		Last Modified: Tue, 07 Jan 2025 03:19:44 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65460abc69cd817e847b20eb60fbaade63fb6212641242c7b0e59012bf869617`  
		Last Modified: Tue, 07 Jan 2025 03:19:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90861f5f649af5e00b6d3eb957399beee29cfdb1109d5463ae2eb1993e5e1ffc`  
		Last Modified: Tue, 07 Jan 2025 03:19:48 GMT  
		Size: 101.3 MB (101349757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02835df1861d01241b7c59a3f08b461c18623e07635e33c92050739bd6f96a6c`  
		Last Modified: Tue, 07 Jan 2025 03:19:45 GMT  
		Size: 8.7 KB (8683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c3eea49f830e108d9ca9de81e932742542ed6cd3aad5ea916941620635bd75`  
		Last Modified: Tue, 07 Jan 2025 03:19:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0d44894c2f201cc19d18f09a144d0f83a8d86483f7246d6dab47d377449689`  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3baf58a6375dc8a7777b3f11f77a38a9425b2178e158a096f348f5110506cc65`  
		Last Modified: Tue, 07 Jan 2025 03:19:46 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6448aaf17cc759617155c0dd9233274b6c6ac525a6fb6ac8b092eab45b379107`  
		Last Modified: Tue, 07 Jan 2025 03:19:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:842d894dba2383034d887b71dd14c76ec49307bb386f47df4734751e3abf19f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.4 KB (637421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c9efd4872b28f6523037ff0e9a64294d236266b4202fe3590e34c335fbf4ec`

```dockerfile
```

-	Layers:
	-	`sha256:f1d33a928373e081bd9543736b2b67c6db6729e2629a3e9058af451d7dfb2255`  
		Last Modified: Tue, 07 Jan 2025 03:19:44 GMT  
		Size: 592.1 KB (592105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4012ebe45f085f3331d66cc2d17d5f4ee2623856d6c9021a754133e05d3a0ecb`  
		Last Modified: Tue, 07 Jan 2025 03:19:44 GMT  
		Size: 45.3 KB (45316 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:9375c793fa880ac63ddfbbfd48efce69fd15b216285a1f222a051a6904ab8640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85891635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630c87c1d0f39b38eee00a0ca080d4d8944173868d76dd414fb48644585754b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=12
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=12.22
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=8df3c0474782589d3c6f374b5133b1bd14d168086edbc13c6e72e67dd4527a3b
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de96468eece71c85f4bb0a7999811760df319dbf27297c93b5400d808010b8d`  
		Last Modified: Tue, 07 Jan 2025 19:34:36 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ef862e296f72156a9359f03496068907da4d96d0508278541e6a7d0e39059`  
		Last Modified: Tue, 07 Jan 2025 19:34:36 GMT  
		Size: 1.1 MB (1082166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c94277577924b774023dd7b724eb96608b5ca33b3f94ab81c9a5c92b1cd283`  
		Last Modified: Tue, 07 Jan 2025 19:42:07 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeb06c72d32f098e8a54cb3efec1981334893662c4f86eaf4109b46c6ab57e6`  
		Last Modified: Tue, 07 Jan 2025 19:42:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4165a0dd16f664e66f7789d70fd2eeff88f523baaae70a0c235791a443c81449`  
		Last Modified: Tue, 07 Jan 2025 20:12:43 GMT  
		Size: 81.4 MB (81432573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ec2038940165a769b2b007e671f38e2b35a402c221762cf6554956ef4de027`  
		Last Modified: Tue, 07 Jan 2025 20:12:41 GMT  
		Size: 8.7 KB (8686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68486aaa4eee044424579305a630dd5b99623ab4f176dd1318cfd3ad21a0961b`  
		Last Modified: Tue, 07 Jan 2025 20:12:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7da87c4e7282880ce2e4724c1aed235e1deae21b540e42e7efd0a6b2b89689`  
		Last Modified: Tue, 07 Jan 2025 20:12:41 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2f64f49826cce1c18931aa91f1bd57177dde2d030d7e9e820405be4fe15142`  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b94ac3d61b810c4f917fd56019ee1776b201de6f5483f2faa84a282573ff18`  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:d3f8f01a4a104c820038dd9b5ef8c7fd70c2141a08c9896926b1159fe5a40d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 KB (45274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081e268f3f2ed5e4bf61c93c6f8bea8bfa6a2a2bd8494ea4add10bab95bd0d84`

```dockerfile
```

-	Layers:
	-	`sha256:4bb53cbd67785d88cb76494f8ee9df19437fa7f54497f309915b659f7dce8a24`  
		Last Modified: Tue, 07 Jan 2025 20:12:41 GMT  
		Size: 45.3 KB (45274 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:e62f09cb6811bf3ac7eece52bf6e53c98a8785d3e9725101a62a8d2d9c4cc14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81198813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba9640765373f320332ce5ce18cc3aeb2b207e2276dfee496e68896626796f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=12
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=12.22
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=8df3c0474782589d3c6f374b5133b1bd14d168086edbc13c6e72e67dd4527a3b
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Last Modified: Tue, 07 Jan 2025 02:55:27 GMT  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07afa41536400af4ea50e45d7d4f3f17c8f9f2441b2f3acffcdea200b4b8484a`  
		Last Modified: Tue, 07 Jan 2025 20:01:51 GMT  
		Size: 981.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac50e87c937aebaa1bb04f32861d37fb63b2a439efdb973c652975fbfb63c014`  
		Last Modified: Tue, 07 Jan 2025 20:01:51 GMT  
		Size: 1.1 MB (1082164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8f9cfa8c61c9ec55f7c05e411c53508e64d9c896be497bf5cb8ebe95508544`  
		Last Modified: Tue, 07 Jan 2025 20:11:18 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8918d3fe9f630f4883936b2a531fea989dfb5bd8c9cd370908ed7b81c5d98f53`  
		Last Modified: Tue, 07 Jan 2025 20:11:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f839d2faff03d763479799bac433b4a41c7640c95e94472bab1dc11ca3fdf1f7`  
		Last Modified: Tue, 07 Jan 2025 20:37:25 GMT  
		Size: 77.0 MB (77007550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce96aa0d344784bcd1f8592ca33e5b13aabd17d48e1fe88bbd81af838bc2294`  
		Last Modified: Tue, 07 Jan 2025 20:37:22 GMT  
		Size: 8.7 KB (8685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345300f5d33d9b17790cf9eba1ac8f437c8086ced44549d123a365455f78c872`  
		Last Modified: Tue, 07 Jan 2025 20:37:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bab846328d6eca3e26736b7c5f7d0235b8e3562e4688e22f0e82cad2971402e`  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f3b351b8d14412a916a43fb88c332881f1841483afd828425741548effbc41`  
		Last Modified: Tue, 07 Jan 2025 20:37:23 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03495a1762cee7f3b64300d59e7bbc9a765cf7309630ac3d1912adf97fe67789`  
		Last Modified: Tue, 07 Jan 2025 20:37:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:ff2637dbea5d7fc7aa6a7e5efb13b2e3e71c6315d58a0f1fe3e942602be9d6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.6 KB (637631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bb3cae3c348b562a253f203bf65c1b26a3f2728380d0b4b68e23801c386e1e`

```dockerfile
```

-	Layers:
	-	`sha256:e4439dc0a9fa12e326e3714f8dd67076b784b187a288222c352d99af5aead9e4`  
		Last Modified: Tue, 07 Jan 2025 20:37:22 GMT  
		Size: 592.1 KB (592141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43a2a91e5788e406e5d640bfc6e95fd1511e44519e3b675354adfca095f0d8c2`  
		Last Modified: Tue, 07 Jan 2025 20:37:22 GMT  
		Size: 45.5 KB (45490 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:992831ecb85c25f0b306b554d7efb91b18b1ec541e97394b5a7877b1223df102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102040772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f355b757819de0ec307746c8593e113dbbf371b98c9824da67379394cd0d695a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=12
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=12.22
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=8df3c0474782589d3c6f374b5133b1bd14d168086edbc13c6e72e67dd4527a3b
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc885904e6ef2a23957b7ed26ffaee5cc7f004763f8f5e620ade626fdc81d566`  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0087acf4148de1bab79af0fd578df391a52e76a01af3d0e36c8c213ee3f82a8`  
		Last Modified: Tue, 07 Jan 2025 17:50:53 GMT  
		Size: 1.0 MB (1041722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23274993fc45e922d1d26b3fb095be284cdc003f231e43134ba9fc5da7b7c9b2`  
		Last Modified: Tue, 07 Jan 2025 17:57:18 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecad913ed4d0dbf84201f9d6a7901ec125705232dc4fa1dd12009d9937d0099c`  
		Last Modified: Tue, 07 Jan 2025 17:57:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6793854e552b25d4fe1cc4766318ec5d21949885200d065669345392ab81a56`  
		Last Modified: Tue, 07 Jan 2025 18:20:34 GMT  
		Size: 97.0 MB (97000187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da0bce290a10475dfde1cc21d835ef1b82b3dd2dcd5b0f9e90b7b9ac567897b`  
		Last Modified: Tue, 07 Jan 2025 18:20:31 GMT  
		Size: 8.7 KB (8685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8059d19e0c2eb8c9181458c5c19c36777a47d634481af5157e0b06bbcf2717c`  
		Last Modified: Tue, 07 Jan 2025 18:20:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c079aaf07cfd69678b1223c79fdb2d88e4c283012e79191a829a2881148771a`  
		Last Modified: Tue, 07 Jan 2025 18:20:31 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b264040d4c401233876acd8d63bc987c0811fcb53662caf7351b4bd7ebc6371b`  
		Last Modified: Tue, 07 Jan 2025 18:20:32 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b983c36fe00b96ed70c4f72381c0a59bda39e0f49a02f05e06598781fdc5a5`  
		Last Modified: Tue, 07 Jan 2025 18:20:32 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:458a284a84ea1832e0cb90d6d461f04dc091cb2111157d5de51151af688af074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.7 KB (637695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e5562260c144c41907fb6602b071ed55e4891d107ff5495d5bc212266ce8c9`

```dockerfile
```

-	Layers:
	-	`sha256:7ac50a1f130a3902a3795408cc67acf930c43ea8b60f89a6ee478d04c8523de6`  
		Last Modified: Tue, 07 Jan 2025 18:20:31 GMT  
		Size: 592.2 KB (592161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f647896bd47e9e4c4274ada4da930c116de573e86b6a5c1b385843f8ab03797`  
		Last Modified: Tue, 07 Jan 2025 18:20:31 GMT  
		Size: 45.5 KB (45534 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; 386

```console
$ docker pull postgres@sha256:0b10a7ffbe97bd8f09ee5a442649a3e3c37c98c6be0aaa4a543a7bee5a04b202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112177797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6790478103d849125e8fb35d16d0a6db4e5eb175af1edc773fa8000c812360`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.21.1-x86.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=12
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=12.22
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=8df3c0474782589d3c6f374b5133b1bd14d168086edbc13c6e72e67dd4527a3b
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1b51cef20fac755ea70acf005c7461407387b0deae88500e38a1982868469f7a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3458271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec4163bcceb4d57fcd9731df072fbd8be0dd2b9c79cd649baa0b7de67239c92`  
		Last Modified: Tue, 07 Jan 2025 03:19:38 GMT  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f52a3897e30475219421a4e4bc5ee92ff6cb0edd93b4cd95675dd4a635bb23`  
		Last Modified: Tue, 07 Jan 2025 03:19:38 GMT  
		Size: 1.1 MB (1089821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7797a3fac6903e4a62cae36d209bed2465903de6eaa00531102f66f9ad562428`  
		Last Modified: Tue, 07 Jan 2025 03:19:38 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5418215a3ca7282712c468fe178ce53f91fa2a76771b46bd09409ff9c908c2`  
		Last Modified: Tue, 07 Jan 2025 03:19:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92347a6f92e971f8502ca2627edd2144c708e790cefc9ff47ef97c57065eebc8`  
		Last Modified: Tue, 07 Jan 2025 03:19:41 GMT  
		Size: 107.6 MB (107613852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a01b5e67cc7d11c4ebf1ba106dce8ad0a9466f35c293e39beda0fde12446a4`  
		Last Modified: Tue, 07 Jan 2025 03:19:38 GMT  
		Size: 8.7 KB (8683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48ae08e858b41d5fb45470c338eee8403c5906e59e3ef862e88f4759851c519`  
		Last Modified: Tue, 07 Jan 2025 03:19:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7284c77e3954c874e30d3dc3a30bfe87923996ae5338e30ba570876d1bc27d4d`  
		Last Modified: Tue, 07 Jan 2025 03:19:39 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d8416508bda814b993cd8b16946292d823ec01676ef0390581b83014233bf6`  
		Last Modified: Tue, 07 Jan 2025 03:19:39 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b52790f624230562f5e98242898fae8f06f309aaf4ae73a3a7cda7866297f5`  
		Last Modified: Tue, 07 Jan 2025 03:19:39 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:c201c08d99778b808d1f4310df93e3fe3653e03b027acf63820ec3594a52e2a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.3 KB (637348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b0b77b5a5074cccd790e2a3a8a51cb3e9a92b315abbccee128600f1009f208d`

```dockerfile
```

-	Layers:
	-	`sha256:d42dc90d320df8213ec6e7fe0aa1ac8ed6d0d1382cda008a887f14d05e55019e`  
		Last Modified: Tue, 07 Jan 2025 03:19:38 GMT  
		Size: 592.1 KB (592080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea70a4545d4094fa4d41d63964cb05978c4eb7adab567f50e086365e35e0f365`  
		Last Modified: Tue, 07 Jan 2025 03:19:38 GMT  
		Size: 45.3 KB (45268 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:ad3cfd7ae57e7a563bfdf448cc066ac006344cdc221cd1dada4571a22e269a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89608619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f64287e04576280ce8dfa4e19c398a213cbf58ae1518267dfd1b9a43a82417d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=12
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=12.22
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=8df3c0474782589d3c6f374b5133b1bd14d168086edbc13c6e72e67dd4527a3b
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Wed, 08 Jan 2025 04:50:40 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a0896a286963d63a37b6bd51916fe939b0c6315e74819aec35d4e627c0a8c3`  
		Size: 978.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b15c203761984bcd620e4a66c0adb8ac7fd47d64bc9f81428049641c9ad9a8`  
		Last Modified: Tue, 07 Jan 2025 15:19:36 GMT  
		Size: 1.0 MB (1029917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc88ce32ee8d127dc1c16b988d7912961a31bfd3e9a4800814423df182108f9`  
		Last Modified: Tue, 07 Jan 2025 15:19:35 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8777a3577bad1a46298b2e1b4be891134aed7de4d24f73cb59f653af35b6f2d2`  
		Last Modified: Tue, 07 Jan 2025 15:19:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12766e179be4531891ee698cb9d1d2099d6f1945883be55b17195e753af23e48`  
		Last Modified: Tue, 07 Jan 2025 15:40:25 GMT  
		Size: 85.0 MB (84995093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0d59bfab55fe4c368f391a35c70abab0319974f1ee1a43f7f4e9c947c3cab1`  
		Last Modified: Wed, 08 Jan 2025 05:51:34 GMT  
		Size: 8.7 KB (8692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d46ac6edab390da7a8652b31b54569c7ea10033e1bb3e0e241454cdeaea315`  
		Last Modified: Tue, 07 Jan 2025 15:40:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d85fe34ea9cf42f913a3687282e53244d5258708f49a21cd1ca0cbecfc815a`  
		Last Modified: Tue, 07 Jan 2025 15:40:22 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1b935111b2b916d2bf8adf26cdb0892c2406c987fb50eefe8b087ca2032381`  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa02a95fe3fda547b253dcff1cf857067d4f71b433083b37eac03ede2699bef`  
		Last Modified: Tue, 07 Jan 2025 15:40:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:27da6ae5a4d795d399563f23e39138ea7429a9d51ceaf216664acaeeddfd2e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.9 KB (633896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5410788f24068be525dad545f9619463ade7085e9728d282c3ed0ce9782e3fd0`

```dockerfile
```

-	Layers:
	-	`sha256:c3cde31a69d3b54c70cc0135ecbf198cc437ec6cb1c40893d3155286b2601ad6`  
		Last Modified: Tue, 07 Jan 2025 15:40:22 GMT  
		Size: 588.5 KB (588526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff6d03b4564687b9a14d2a1f1989f0e27e5dc3e235aa4fdb9d7997731956fce9`  
		Last Modified: Tue, 07 Jan 2025 15:40:22 GMT  
		Size: 45.4 KB (45370 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:68249a317918f9330ff9feaea7da81151dba355dc9ef1ae9bc42533a872cb9f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105499901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56fa232fe9e1a0d6ed37d70060e34e38ad19b37fef77959e6fed138e185afbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=12
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=12.22
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=8df3c0474782589d3c6f374b5133b1bd14d168086edbc13c6e72e67dd4527a3b
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1dea23fd35b1b2137e20c9f0c7d93cd055d0e7684137991907363db0d39c8b`  
		Last Modified: Tue, 10 Dec 2024 05:44:51 GMT  
		Size: 989.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f737b43c2933d58c075f6d291e04f55dcac95cb1aea8e77dc599e92d07ba38`  
		Last Modified: Tue, 10 Dec 2024 05:44:51 GMT  
		Size: 1.1 MB (1091676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92695bece0326a0b32d46da3fa58055a512403a2afdee3e8b63736282f87e7bb`  
		Last Modified: Tue, 10 Dec 2024 06:39:47 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7283951b183c70757b241796701f97804ece3289850b10110cedd957374fce3b`  
		Last Modified: Tue, 10 Dec 2024 06:39:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd50d08b162682d1ff7e7ecff05bd1e33eb7e27f1ef801afecae97e063df3b8`  
		Size: 101.0 MB (101038326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad6d2235ea581e692df619c9247cc5c8c044a2aa18835c98f42a45e77e5c6c0`  
		Last Modified: Tue, 10 Dec 2024 10:05:27 GMT  
		Size: 8.7 KB (8692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4792955602f48bd8a548df0f77a0489b1bf43db219a9cf1fe9bd88446812e9a0`  
		Last Modified: Tue, 10 Dec 2024 10:05:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b01eccacf57266f7ca530a2e7fe997f09ee27f6632608513cdd162d8ffc48b`  
		Last Modified: Tue, 10 Dec 2024 10:05:27 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3272d3bb4c0d19ea6cd9def559c5a64225468a92f8fef625fbfa0fc55248ad`  
		Last Modified: Tue, 10 Dec 2024 10:05:28 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2e0d83de02099f66907bfdec6c7b866bc61f2d01794a9f352621b29596d2fe`  
		Last Modified: Tue, 10 Dec 2024 10:05:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:8bd1149fc9d6f4663a8f531fd7cc6305ad317b929170e6bd4156b082258b938c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.4 KB (636411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44106da3f5c78aad808ae1b0a7d047b47146a730cc2a66578f487b56a6244657`

```dockerfile
```

-	Layers:
	-	`sha256:abdaa6d339a4ccedf1145043d99f8814870ee63adff41a6e46e53bc23a3bb11c`  
		Last Modified: Tue, 10 Dec 2024 10:05:27 GMT  
		Size: 591.0 KB (591035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ff0aca1088f4e84345dd5fa79a930c989f2cff1fa6e8e0034eb8da3432a4da`  
		Last Modified: Tue, 10 Dec 2024 10:05:27 GMT  
		Size: 45.4 KB (45376 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:fb37b12bbfb544c1a404552807b9e1b014c963ea8abf739afbff091207791713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114440458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a0c82c7a3ba666c4678d98125f2c76ad8ac71fe447b8c05f445c1895e794302`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=12
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=12.22
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=8df3c0474782589d3c6f374b5133b1bd14d168086edbc13c6e72e67dd4527a3b
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57ba6a48bedebfbd70a5136971e0142b2813340a67dafab281a19ef0804a967`  
		Last Modified: Tue, 07 Jan 2025 17:32:17 GMT  
		Size: 982.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38b011c64fcc9ed918362f86cd977f29caf9b15d32a70238eeaebec9912df16`  
		Size: 1.1 MB (1079916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a6f475714d892ae5c8586f9c1d530e40f57f0cf3ce17542bfa88c9a70ced31`  
		Last Modified: Tue, 07 Jan 2025 17:44:39 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2336a7dc32fca1b70859b019f6a4a59c424124a595c51cf822cad024d25a455a`  
		Last Modified: Tue, 07 Jan 2025 17:44:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8410a0306c2a1ce9f425e6e802ad4b15a6c6c2e7355d38cf1b5b4d73bb488462`  
		Last Modified: Tue, 07 Jan 2025 18:17:28 GMT  
		Size: 109.9 MB (109885234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb06cb58990eede400bb920df87a2bcc816b646a646d21d12840d81bc61e42d0`  
		Last Modified: Tue, 07 Jan 2025 18:17:26 GMT  
		Size: 8.7 KB (8686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fb3b3e5e407b457f492a29523281d227f67a9c2f3ab2795c686163433de881`  
		Last Modified: Tue, 07 Jan 2025 18:17:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e614d3ad584a7ddcf8a83425a1db544abd5c2e2fea6c350c5dce38ad6eca76`  
		Last Modified: Tue, 07 Jan 2025 18:17:26 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcae5b3d43400e849f076a6daa1ab52c898a1affbe0230a21278dcd08e3b7068`  
		Last Modified: Tue, 07 Jan 2025 18:17:27 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d43cc5b30669761ae8961c9693e9eb07045ab9b564d568f933961cedfdddad4`  
		Last Modified: Tue, 07 Jan 2025 18:17:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:f9eb0a0224f97430bba9e5fc809821d9e0d8a7240e0c872e96a3bfd8535f7ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.5 KB (635469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0b7aaf862357e2b7b4fdc9a781973149f461e94160d45f798f0175eeb00a36`

```dockerfile
```

-	Layers:
	-	`sha256:efda50ac0711f2d797d93fa0baec7d9cff2ce60f5fd177ed3001ed8282125dfa`  
		Last Modified: Tue, 07 Jan 2025 18:17:26 GMT  
		Size: 590.2 KB (590154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c7d50db6288d34ca373e75c585ba119a1747a99a51ac1afc4cd84d4f9a91b9f`  
		Last Modified: Tue, 07 Jan 2025 18:17:26 GMT  
		Size: 45.3 KB (45315 bytes)  
		MIME: application/vnd.in-toto+json
