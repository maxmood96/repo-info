## `postgres:15-alpine3.19`

```console
$ docker pull postgres@sha256:fa73e46c2c374f1b9faeed55898590747ee6f7cd6480554c0f34fdc7f5232524
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `postgres:15-alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:517a1a029df2810f70972f635b1967a40bcaaa39f397861ffdcb038549221d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98055494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bd7834ab21ed8b7dc46dd41227aa2f1856881d9ac427282a6d3073e8cc18fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:20:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PG_MAJOR=15
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PG_VERSION=15.9
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PG_SHA256=74f2d4565035f0cf729ecb059949faaf1102cbd93759b359822f98f82198c783
# Thu, 14 Nov 2024 19:20:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:20:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:20:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:20:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:20:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:20:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef0fa03e89c1e3834c3d60caef1c9f1c5cebf8d6c7e9707408a0f57b0ffe7c7`  
		Last Modified: Thu, 14 Nov 2024 21:10:53 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af63af786db3eda0c34fb771fac84fae70ae4283cc1e101bda6d4096e53f3c2b`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.1 MB (1120285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a518257191ff416105bec74d3c70372e3455654b1dc134ca5c52b0fa3923e5d4`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31d39284f7b33fda4009709db4acd3b4055b5a6100ab64ec9346a6db74a9ce0`  
		Last Modified: Thu, 14 Nov 2024 21:07:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465acbc85960d6c23ba2d2da4a3707b81ea9048f48cc9126247e51f365adbfd7`  
		Last Modified: Thu, 14 Nov 2024 21:11:07 GMT  
		Size: 93.5 MB (93498575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba7f8dc8610e69af9458d20ff308cdec825d73a71165fe6a3fded6238fb2b79`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318f5dc7ef58234f060cde1ea650f7ba47b1a742d4f506a6974259422af6dfa4`  
		Last Modified: Thu, 14 Nov 2024 21:11:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13ef5124a5969c65adb36e3f2092ef88198f9f1fd774fd2334866f2b6bc11dc`  
		Last Modified: Thu, 14 Nov 2024 21:11:05 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddd9e22ae916d4b8c854a733d2bff4615cf13440e2d18bfe8c6f51fed374f91`  
		Last Modified: Thu, 14 Nov 2024 21:11:05 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9bdbdb8d7355b5e2fbe0e123f101343f1a7a6f4ae8a84f09af0723f52bd99c`  
		Last Modified: Thu, 14 Nov 2024 21:11:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:7d43f8c1d92f2fb6ab8ba194ed104e03bccceb0c9e3c8c281b84b9ad5e0d7fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e30a69102fd77248c31a349b957dbadb5d67edbab1851ecf5d0a1209565b4b`

```dockerfile
```

-	Layers:
	-	`sha256:8d9b175b3f1292e95daeca0d331e1f11f0f5fdd304c9b407de0056a784e52d39`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 969.0 KB (968999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f58c9ed95210080f6cd492c32c0e904e5d9ffc40887027f0e7237ed488791a4`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 45.3 KB (45291 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:9002af78e1a497720851bdd3dbb3cb2a73344ef902c6999abd04e0d99c334d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96491510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1186bc2ed350e51dd0a9662cae548878bb7fa8d76b4bdfd1f0d5d2ee7d8718`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:20:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PG_MAJOR=15
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PG_VERSION=15.9
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PG_SHA256=74f2d4565035f0cf729ecb059949faaf1102cbd93759b359822f98f82198c783
# Thu, 14 Nov 2024 19:20:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:20:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:20:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:20:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:20:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:20:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1129eba1c516693bf2f340f0343f658e37e7812832c7f2e7493ce214856d3fc0`  
		Last Modified: Tue, 12 Nov 2024 05:41:41 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1855f1ed4c4392b8709ed6c84e2a119012e83c080f39bb8faf7f1bbc735a9252`  
		Last Modified: Tue, 12 Nov 2024 05:41:41 GMT  
		Size: 1.1 MB (1086678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255e16740a45a54b3ba44f9bce09b1f67b316dd94e12dc4ddfcfe274678036ac`  
		Last Modified: Tue, 12 Nov 2024 05:49:37 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8874dbe6c02989a5e3c4a6f7b2a59292b8f32afd21211d3933902093d814455`  
		Last Modified: Tue, 12 Nov 2024 05:49:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5076c3e26ff14258701f79eb33da401f80d8ab3e96cdbb45bf84ab998215e0`  
		Last Modified: Thu, 14 Nov 2024 21:29:18 GMT  
		Size: 92.2 MB (92211486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c9f00d5e8abfba94381c75651df6314d4677af3f180281f25416181a45d375`  
		Last Modified: Thu, 14 Nov 2024 21:29:14 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc762952e841c7782f8cec578b936097118937fb2379e0ae6d0720bd698ccad9`  
		Last Modified: Thu, 14 Nov 2024 21:29:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5f203eacb24ebab7952ef3a4b4605eaaefac6631862e4096ebd85262218769`  
		Last Modified: Thu, 14 Nov 2024 21:29:15 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53639175c3cc84ba5d597050f17300af3836ad0f5f9d35d6517ef54bcb4f1684`  
		Last Modified: Thu, 14 Nov 2024 21:29:15 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4464843456e18a7bb04977e0d1d212a92a8f93d646c573404fe085abc3a262a2`  
		Last Modified: Thu, 14 Nov 2024 21:29:15 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:dede4fd011dae4f8058e291cd93e120ef2a0ac7bb4535934bfad0dc0714dce44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 KB (45240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f506ceac2eb4af733de2c5acba3d96c59b0d2b3e0f16792e398e79a6f56d7a`

```dockerfile
```

-	Layers:
	-	`sha256:ee50f937bb79341bb08043b20d6d393dc7a3f58d9ab7484b5a8aea31a9cb5c20`  
		Last Modified: Thu, 14 Nov 2024 21:29:14 GMT  
		Size: 45.2 KB (45240 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:420ba71e788f17d18e6e372f4de4abfc32d07f6e17a9528ef0fc98669c8843d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90822006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be6302a12294588bcef5550e436cfbee93151f69c0f5b33244cd801a4e1f3b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:20:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PG_MAJOR=15
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PG_VERSION=15.9
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PG_SHA256=74f2d4565035f0cf729ecb059949faaf1102cbd93759b359822f98f82198c783
# Thu, 14 Nov 2024 19:20:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:20:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:20:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:20:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:20:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:20:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:02dfd5e2e7e47e8d8f9020a0d7f4d8240d6646afc6a52b168c0899bc0c3d06a3`  
		Last Modified: Mon, 09 Sep 2024 07:03:23 GMT  
		Size: 2.9 MB (2927731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5db41ad436d5f7ebd4024d28883a253bc45e3577ec71b917f3af8f6247e0a49`  
		Last Modified: Tue, 12 Nov 2024 11:50:40 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ec4ab37e54f1eaa5a6a0648af6ccfa09df4dda8aebd4bfd4c95a09aeeaf220`  
		Last Modified: Tue, 12 Nov 2024 11:50:41 GMT  
		Size: 1.1 MB (1086691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694d2ecd365071d47a25ce95fec93acb0830747395eb32752556c88eb3dc3a81`  
		Last Modified: Tue, 12 Nov 2024 12:37:58 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a6ddb81e5151f0e21e0c3fd043dcd36f52e92d27d808d8967dacc037ccb4ca`  
		Last Modified: Tue, 12 Nov 2024 12:37:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847d4667dd47f04c256fb671b8030b436b0771443ce074fdbd8ca3276f4d6aca`  
		Last Modified: Thu, 14 Nov 2024 23:04:37 GMT  
		Size: 86.8 MB (86790676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbada655b51fa048d9d968fde6e159930c3014a7c6dde4fc2d8996c0dc0845d`  
		Last Modified: Thu, 14 Nov 2024 23:04:34 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1500eb0a934ad34eaf9f7786e60bd6ace0735c8a7b3256d908ed195dcd683766`  
		Last Modified: Thu, 14 Nov 2024 23:04:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7e7fdd7ed4bcb34d26bb7a98171d44573732f5ec83c2056946ecec5de23186`  
		Last Modified: Thu, 14 Nov 2024 23:04:34 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05663c9daa7012e72ee519228a80eafd6fbefe38bae9ada2ad2666d842455d28`  
		Last Modified: Thu, 14 Nov 2024 23:04:35 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0907ffd8c7f30989a343b3f4bcdb75bb1c9a51ff5aa579a5ebc7a5894eb2f962`  
		Last Modified: Thu, 14 Nov 2024 23:04:35 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:293da1b8ba73124001e00db2079203d54abfb7d6714db8235fd8ac1be4edd098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dca74dac383a5e97c193ce59e63372fa0e9f7704197f3f4eb985a84eadb79a3`

```dockerfile
```

-	Layers:
	-	`sha256:379ac54b1f41421392a80607a1eebe4ed9c8966d6ae75c8a73c34c353651bb5a`  
		Last Modified: Thu, 14 Nov 2024 23:04:35 GMT  
		Size: 969.0 KB (969019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:701ca1e474ac897e951eeacaa9837eef70311afad2428d08f809c1327296ce45`  
		Last Modified: Thu, 14 Nov 2024 23:04:34 GMT  
		Size: 45.5 KB (45455 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:24dc8f6aa9037edc49cb72869076d3f02b139e4dd0a89418818d0eb8caef9d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96662494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f2be7b9bc3ca3ef4ae10f1106abf299a685bdec1d1b9cbf98f0b4da5551bdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:20:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PG_MAJOR=15
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PG_VERSION=15.9
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PG_SHA256=74f2d4565035f0cf729ecb059949faaf1102cbd93759b359822f98f82198c783
# Thu, 14 Nov 2024 19:20:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:20:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:20:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:20:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:20:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:20:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff54d4329846145ee02efd07421e687bf03dccfd110b41d27be9e1b28191499e`  
		Last Modified: Tue, 12 Nov 2024 09:17:39 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad02ddf5c8ac009520c934fddaba6a040ac5e2d873f745a521aa4ac96362cc97`  
		Last Modified: Tue, 12 Nov 2024 09:17:39 GMT  
		Size: 1.0 MB (1049359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5499e4800cc0b00cf4179471fd03a5783f73a1e3c78a01d0d1b17fcd199b8b9`  
		Last Modified: Tue, 12 Nov 2024 09:25:38 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f0d3586ef1d035ecc3b6ea69d4e665fbd7fc01f5c485dd1dc1f871e85f4f0d`  
		Last Modified: Tue, 12 Nov 2024 09:25:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ae4d492fb5f17e28c8d55f4e51eac9710c4317cdce114132b8d3e721c31183`  
		Last Modified: Thu, 14 Nov 2024 21:30:42 GMT  
		Size: 92.2 MB (92236984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6167666ba9ee57efb25372ba3e2f4d94292ba14e9f2860a334db2adfefce79`  
		Last Modified: Thu, 14 Nov 2024 21:30:39 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6659a551764dd392e1c2c50f895a96c325aadc192697ac9a623351520949fb`  
		Last Modified: Thu, 14 Nov 2024 21:30:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b7f52268e7a22f07781ba12b689c550d7592a075926e26626d0da6ed1fe72`  
		Last Modified: Thu, 14 Nov 2024 21:30:39 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2054bc167d1153e3e00586b3bfb1055619fa2f7a6bd49d9b54c3fbbf8564479d`  
		Last Modified: Thu, 14 Nov 2024 21:30:40 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f77e80992dcf647dcaf0258ecb2fbf7c77d82395eeb924c5d0bbc9db78cbad5`  
		Last Modified: Thu, 14 Nov 2024 21:30:40 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:6e8c0b12be9266c5f5ece10f7775227bd89e2d359035057b56d15074b8a220c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d38472bc24597d824794ab965dd88a0085677279ce666f97b58e4c29cee6c30`

```dockerfile
```

-	Layers:
	-	`sha256:f98e356084241874cd9600b43cae9669b25f7f278b08a3aec0bdce831475b0db`  
		Last Modified: Thu, 14 Nov 2024 21:30:39 GMT  
		Size: 969.0 KB (969031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1fda6b9f0180ac96624cf55a2023f5c19ae74f36cbc8afc52ab47c1b596a006`  
		Last Modified: Thu, 14 Nov 2024 21:30:39 GMT  
		Size: 45.5 KB (45491 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:a6ca4be2931b64da073104a847e113d431c4bffe0f2bf0b6c61f3832db8e5ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103191991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df895d850b8cef5e7fd40981a716f61fdb768fe237d8cea799869e612467d343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:20:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PG_MAJOR=15
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PG_VERSION=15.9
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PG_SHA256=74f2d4565035f0cf729ecb059949faaf1102cbd93759b359822f98f82198c783
# Thu, 14 Nov 2024 19:20:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:20:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:20:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:20:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:20:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:20:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac083ac39ae67da31581ceef8cc71aedef414ec86a9297da8a561010e9c1f0ab`  
		Last Modified: Thu, 14 Nov 2024 21:11:49 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64549c9d4220f792100f7d2c6f448e4515dae53d59b30f12c102f43a46f19778`  
		Last Modified: Thu, 14 Nov 2024 21:11:49 GMT  
		Size: 1.1 MB (1095469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959cd599b2a98df0cf0bc4eaa59b68083caa66a7a5ee74a82c5b001421bf9614`  
		Last Modified: Thu, 14 Nov 2024 21:11:49 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc292b111350836465a7c7d8f1b8dfb34ad39b5e4f18016ed284ab473e3fd89`  
		Last Modified: Thu, 14 Nov 2024 21:07:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651edf06c946abfd1760f2f403a86032d8fb58da197157d5ea2bfc6aeaaa1359`  
		Last Modified: Thu, 14 Nov 2024 21:11:53 GMT  
		Size: 98.8 MB (98825959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61eb2985647e37f4c0c5e77be23cbf8c6dcb80f0a1d1b981002ab9b1b2290a0`  
		Last Modified: Thu, 14 Nov 2024 21:11:50 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0c8d5039340e26863d9bb23c3a4af893df808bbece7e7cf15bbdda3adc00c1`  
		Last Modified: Thu, 14 Nov 2024 21:11:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d786c0b18b87d7399f3ba28b407b9c09d976826d2915fd0dfad1f75fff43aab7`  
		Last Modified: Thu, 14 Nov 2024 21:11:50 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5140d60d69378a48ef7114ef0680de3b75967031cf8dcfd8b1bb7b7e62009685`  
		Last Modified: Thu, 14 Nov 2024 21:11:51 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723c6ff92e02677c445f04cce808b09bc5b36c32fbf732c40d0b73f4aed84e85`  
		Last Modified: Thu, 14 Nov 2024 21:11:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:a1d5bceba4aba655a226d4703e9c5a96b404a966cba1075f40a89c25fc2cb2ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05bd1013f04bcdc08090926bfc48f4bdb08867b2e7cdedc694b34dedf7714ca7`

```dockerfile
```

-	Layers:
	-	`sha256:45cb3567550e56d6b4283960730af6679683d882a20fbf5c4870484deae8db0c`  
		Last Modified: Thu, 14 Nov 2024 21:11:49 GMT  
		Size: 969.0 KB (968984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a054125fcfec7b76cd4603a40f091c0ff1393c79cb36b0db14f38b432f80c02e`  
		Last Modified: Thu, 14 Nov 2024 21:11:49 GMT  
		Size: 45.3 KB (45253 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:077ab2003c8598878c2cf3aa001145e080ef0b02f896bc36dc7412d606f333d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102477928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07bee97a69afe5e146aac60d05d53117a019c1ae80c20f7ca85b5857704786b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:20:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PG_MAJOR=15
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PG_VERSION=15.9
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PG_SHA256=74f2d4565035f0cf729ecb059949faaf1102cbd93759b359822f98f82198c783
# Thu, 14 Nov 2024 19:20:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:20:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:20:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:20:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:20:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:20:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44aed1596aae53b43b5c560a70ed3077f01224dad331cd0f195462cd93de112`  
		Last Modified: Tue, 12 Nov 2024 07:04:17 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0c1eec1649b1b27928c826ff7967e09692327c62f6641f0fb1010c2e92117e`  
		Last Modified: Tue, 12 Nov 2024 07:04:18 GMT  
		Size: 1.0 MB (1039697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ad50198d9aa09c32245fbf4ebc775137c6396b849af754b3cb0958d7b808ae`  
		Last Modified: Tue, 12 Nov 2024 07:13:05 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d730f1e31929ec96a765b66b931f5f6ee89769f0e4ad0de920de3c467d6977`  
		Last Modified: Tue, 12 Nov 2024 07:13:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1aad38faa4cfc97f2b60a4cc52d7f0a0b51c7f16dad86f740943dbbe7fb345`  
		Last Modified: Thu, 14 Nov 2024 21:34:53 GMT  
		Size: 98.1 MB (98056814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee14a4008ec87553edf11506ce294e9fc5c4f2946c7858e549966e4db5ea66ec`  
		Last Modified: Thu, 14 Nov 2024 21:34:50 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29443ed98b118de8ed0250a2cc359e297ed53d0cbd692260bd3ee56130ad9453`  
		Last Modified: Thu, 14 Nov 2024 21:34:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7441a8fe7abeb61ebb01ee5f4b001686a77ea582ee3c0db3e3f8b11658f1e89f`  
		Last Modified: Thu, 14 Nov 2024 21:34:50 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ce9f95054e6a937d223771d5ae7c3de977a123ee84cea1cd20faa476cb7540`  
		Last Modified: Thu, 14 Nov 2024 21:34:51 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19aac577d35c604849f3999f2f25c6f5fdf0b73592f8a162724540dc0a4caff`  
		Last Modified: Thu, 14 Nov 2024 21:34:51 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:2858579e3f5912d00d3af773fdd8f00cb139bb305f5f892167df78050374c00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a8d0e7078fd96acc6e0302dece8c52cdfb12a53cf2325d1fe71b9a256121e2`

```dockerfile
```

-	Layers:
	-	`sha256:1758782700b10eab0997c88afab35f8dadd069029da2f90a7797468e5cf9717d`  
		Last Modified: Thu, 14 Nov 2024 21:34:50 GMT  
		Size: 965.4 KB (965403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eccc92f83d791c626d156343c9d4880468abc4a1b93be7668a5ea5bc80b42c9`  
		Last Modified: Thu, 14 Nov 2024 21:34:50 GMT  
		Size: 45.3 KB (45339 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:2b45ab6c48f5a1a6ef3aadf5c865cf6bffa67b6519287170e0349afc870bdcd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106707591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:860a1c9fb1933411816203652522204a3da9d260a808dc67044e6526e6d4f4ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:20:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PG_MAJOR=15
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PG_VERSION=15.9
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PG_SHA256=74f2d4565035f0cf729ecb059949faaf1102cbd93759b359822f98f82198c783
# Thu, 14 Nov 2024 19:20:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:20:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:20:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:20:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:20:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:20:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:20:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be5dc1246d0976e782f1978d2b2c680cd917af96a6f248e327cf6c5a71ddbac`  
		Last Modified: Tue, 12 Nov 2024 07:39:49 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea0a759c44d4c20668d2dd240b15b5122b742a9976f56b2975b365b6c05623a`  
		Last Modified: Tue, 12 Nov 2024 07:39:49 GMT  
		Size: 1.1 MB (1083901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca36db6f4d56245ca10555850fe42a93b94514e3a413dfee1561b0bf0ad39e3d`  
		Last Modified: Tue, 12 Nov 2024 07:49:09 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fa16f70538566b10dbb068814b0148bb3126bf49f5e2f7a00b9a0be1ef603b`  
		Last Modified: Tue, 12 Nov 2024 07:49:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12570155043ec60a9508900f0a5ea2ab45a8aba093d14954bf316ec76a171bc1`  
		Last Modified: Thu, 14 Nov 2024 21:50:35 GMT  
		Size: 102.4 MB (102353366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd0464a3923264f6780041cb56457b49860df7aa694a6271e5c8e4c7cff80d6`  
		Last Modified: Thu, 14 Nov 2024 21:50:33 GMT  
		Size: 9.5 KB (9456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51529d58439fdbbf4e3a47fd2f475a8a91ca63ebb00a8a7a4cda483b9976abdb`  
		Last Modified: Thu, 14 Nov 2024 21:50:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab08eeba9ee7a578121a96b80d79bd420afd2a8203b3d7df193ba1b9ba4f1ae`  
		Last Modified: Thu, 14 Nov 2024 21:50:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f45d209fe3b8b15abf3467f29cebbd23ee84868b837e5e49c00b5b91886c45`  
		Last Modified: Thu, 14 Nov 2024 21:50:34 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af04403b784569f34724fe93c9c1098a393fcb6a2a5dcc0d2d17dca7d52a51b5`  
		Last Modified: Thu, 14 Nov 2024 21:50:34 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:f16f47c7cd96de6916d9a2b453b1c28583a1db6f5c3f005baa8ed27e760d3395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1012342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8213824e51d1c4b02b06d27b0db905410c03c856a81c767eca47e04d89d6b1b`

```dockerfile
```

-	Layers:
	-	`sha256:74c2fd98ece5ff735656ce5b78e95d8aeac41e6296264087f8f0ef509c6e2834`  
		Last Modified: Thu, 14 Nov 2024 21:50:33 GMT  
		Size: 967.0 KB (967045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b03dd62a6395692ec1cf68d6d41ce8bc289a3eb88d84d86107d5404d90a5bbc3`  
		Last Modified: Thu, 14 Nov 2024 21:50:33 GMT  
		Size: 45.3 KB (45297 bytes)  
		MIME: application/vnd.in-toto+json
