## `postgres:13-alpine`

```console
$ docker pull postgres@sha256:a5b7bcac8ca3650bb50680de05c104d53bf4bccb921aa94d79a2a0b7b6734c65
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

### `postgres:13-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:da0e2541d9aea72d2c0c903a492162ddf35e75a2324dc7d8883f271e9cfe2abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109215348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb2692dad6dc55989412806cd2ed9ed2086beb73f4519ca9e75b49c0cc41143`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
ENV PG_MAJOR=13
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=13.22
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ced3e2d487515942910ffaa07a86b6f49708ad47d81239dad482dee1fdf91d`  
		Last Modified: Wed, 01 Oct 2025 14:07:18 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fa926a72e86c491d8c0609ffd28896facbeb41b4ae8c25c1b16e64980553e8`  
		Last Modified: Wed, 01 Oct 2025 14:07:18 GMT  
		Size: 915.4 KB (915392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e2eb0de7930e548d2a043ba5bcf27e3406f30288cdc7369caba31574f4dad2`  
		Last Modified: Wed, 01 Oct 2025 14:07:17 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f731747b223083da2f4289591f5c8a0e19595fa3fa1ca04d2eb49c4b0d76d12c`  
		Last Modified: Wed, 01 Oct 2025 14:07:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fd8cb3ec2f36106f261c6a831508f6af15a23745b91654f8db991c08c32724`  
		Last Modified: Wed, 01 Oct 2025 14:07:24 GMT  
		Size: 104.5 MB (104483589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f182ab0e17f6c5a1f821eac5e62a45ec1a345c53fb901c596cf995b751b299e6`  
		Last Modified: Wed, 01 Oct 2025 14:07:18 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cf51ddd4f8cd95d97ed2572583d76154d4cdd8289938aee3c7cf9484b41767`  
		Last Modified: Wed, 01 Oct 2025 14:07:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d96f92368fe44f33fb83631bc38aa64af959eab483a00314cf462aed9d1d8d1`  
		Last Modified: Wed, 01 Oct 2025 14:07:18 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087f768a8ccc1f2641211e2e1c6fa2003283a80c65410547ebae475d9bd32f03`  
		Last Modified: Wed, 01 Oct 2025 14:07:19 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a8e5f3036088827deb0e9ff6012fc278289b10fab357c68551b8bf2104afa9`  
		Last Modified: Wed, 01 Oct 2025 14:07:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:dbe6872fb3b06dec6287fcbfc79047827b7de0e95df5f2005e013d7e68e81786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.6 KB (637631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8f5f3e5b72bb8afacb95a7cb64dd93faf9a1f0d5b37654e419a46f881c32fa`

```dockerfile
```

-	Layers:
	-	`sha256:33ea534b46b4bfae08fa100ebf8db35d307e3ae0773d05a834a6cef9bf517f9a`  
		Last Modified: Wed, 01 Oct 2025 14:07:24 GMT  
		Size: 593.8 KB (593802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe88db693b8992b6a7f2ba0521aefea6bbe7d115eab8862649fe73ca4d916375`  
		Last Modified: Wed, 01 Oct 2025 14:07:25 GMT  
		Size: 43.8 KB (43829 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:e2e6abf863de8754f399d4e1bf3206d9786898a90d8cd1c1593ea03e1b315c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88465597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1669a4a0b271a3ffbc41c9d4850c282dc0eadfd539d4dccc54d396ce8d343506`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
ENV PG_MAJOR=13
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=13.22
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4626b575b021dd26efde6fd5beed338723b5c8e0107497ad9366d419b4d203ac`  
		Last Modified: Wed, 01 Oct 2025 01:34:25 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51aee67bf873bd50a476284914ee22eebd1757b0199637706222487b32d5174c`  
		Last Modified: Wed, 01 Oct 2025 00:42:02 GMT  
		Size: 881.8 KB (881760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcabcf47de8f8241644bb98bf5860a03975162e21114d320642492fc2dbfa62c`  
		Last Modified: Wed, 01 Oct 2025 01:36:48 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37de9cff0a4a72cc00d019adaf2a6d7fb630c873f9cfbfd78e39e60ab3fbd4a7`  
		Last Modified: Wed, 01 Oct 2025 01:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e3dec66d9f7b8cb8fd4572d5f8b328b004857a0e5644a1036a37f97f62a780`  
		Last Modified: Wed, 01 Oct 2025 20:08:33 GMT  
		Size: 84.1 MB (84066238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f264c289439bc17332e2714a8cceb9744405585429a96f9f59036f2f2151a11`  
		Last Modified: Wed, 01 Oct 2025 01:36:49 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc141ffd09ac8048a68673ed32653000eb023f2151e79a6b66fba5e9823695f`  
		Last Modified: Wed, 01 Oct 2025 01:36:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb2c2bc76ba69c09b5cfb7dcdaf374192ad1a939ae5239cfc8cbcd1bbc0d649`  
		Last Modified: Wed, 01 Oct 2025 01:36:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d5be46289eaf55efa00b7f05095d24f86cb226a9e206f8a75cc016ecaab79e`  
		Last Modified: Wed, 01 Oct 2025 01:36:48 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749ff6ecd4a32627b87c101c3ccca5ccbede3a0b6272fd1c679a27885e0d7c7d`  
		Last Modified: Wed, 01 Oct 2025 01:36:48 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:76fe0eefc2c3f0da15a2e702bcd7145d3670a265331553e51a38da21b7f1c591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 KB (43790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276e71158cbbbd5610a2ebca048096dcc30c74100989648dae37f2e3b0e08502`

```dockerfile
```

-	Layers:
	-	`sha256:9e8978e66d9333d428c8350620578c8c655624873153df0481e63040eeb51511`  
		Last Modified: Wed, 01 Oct 2025 17:25:13 GMT  
		Size: 43.8 KB (43790 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:39f49528c8ff9672a222165105b0112206852fa783e56ffbbfc4f5bdff3ab3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 MB (83654990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb23167c5d72afd7fbaad1e5de4c48abf1026726d3ebc40461e1f519a043c21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
ENV PG_MAJOR=13
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=13.22
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563fb6ceedc00abea12ba76cda2f479c546fe905989b81ed50721c7d05f7dc26`  
		Last Modified: Tue, 30 Sep 2025 23:18:20 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292b7fe917d0cc631a7149bc651ccb27e306c70cd8d18a5bf171b7281b19f447`  
		Last Modified: Tue, 30 Sep 2025 23:18:20 GMT  
		Size: 881.8 KB (881754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8ca9d93706359c9be39d0f613b3f6cfcd729c161288e1ee861f6cd0904b938`  
		Last Modified: Tue, 30 Sep 2025 23:18:20 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357ab531a614971624c0bb0b3a2c90f81272d1ff18aa8c0c5fb02e834ccaf989`  
		Last Modified: Tue, 30 Sep 2025 23:18:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e6dc17c028cd5e85e1c277ee2a727543c90ac3e2794a35631e6c31fbccb218`  
		Last Modified: Tue, 30 Sep 2025 23:18:27 GMT  
		Size: 79.5 MB (79537512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a6f8cbdd0aa554e920336898a097fbdd758f00133b40abf0c69520703cff63`  
		Last Modified: Tue, 30 Sep 2025 23:18:20 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb89645c56accda59eaee4b49d0e7d9ce4b47b740ea7dacb85553db8a45de942`  
		Last Modified: Tue, 30 Sep 2025 23:18:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd727f5d74b197fd076268674e8cd55d1d35abc890988e69fc170280faf2f7b`  
		Last Modified: Tue, 30 Sep 2025 23:18:21 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de042ecbbd111614a574c8b63bf54f68d4183e75c5ef99cdc80c49512ac9954`  
		Last Modified: Tue, 30 Sep 2025 23:18:21 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17043b5ed266174026d1689664f58c83f7ca4fe69c03f883a136f18a1d5bc5e`  
		Last Modified: Tue, 30 Sep 2025 23:18:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:03581fd1112092b75362fbff385bb670a2f1d473c462214b3199c7d42b6797c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.8 KB (637845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f9ed9c316dcef01c7c1b3e09686b72efb6d01ffddba6a1175f0063db602658`

```dockerfile
```

-	Layers:
	-	`sha256:92871e4f3dd8cfe9071383904d35f5300df8d795c92db76bf20f89b8ac127f11`  
		Last Modified: Wed, 01 Oct 2025 20:07:54 GMT  
		Size: 593.8 KB (593838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1a64eda484c9aa3eef2d71390f2dbb3cdd8b9a7d6251a0411e6cfc6aaaca67c`  
		Last Modified: Wed, 01 Oct 2025 20:07:55 GMT  
		Size: 44.0 KB (44007 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:c57d775fa9448c30743a9010d87b707249f0e999e8493454490a8486f58de5b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105459571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb21792431793ff0c4a69f99d4981cef9197c04b0de09c9a3845dc4fa0ded38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
ENV PG_MAJOR=13
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=13.22
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9888c5c88d31ab6a797499a1e9541695f46901524ad5c0e4eaa11e87cf49a77e`  
		Last Modified: Tue, 30 Sep 2025 23:14:10 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1843535e378f2b54478c7c47387ef91ac195e3caa5a550afbf948dba6e7100c0`  
		Last Modified: Tue, 30 Sep 2025 23:14:10 GMT  
		Size: 869.7 KB (869708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60c7e880495154693597ceb05c0836d3c53ea5d54e9e3ccca1b1329ce3e3a3a`  
		Last Modified: Tue, 30 Sep 2025 23:17:09 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f520211c466b6e70c544f79e9f99308bb390d4e43d780b27cec9af2d9bb193`  
		Last Modified: Tue, 30 Sep 2025 23:17:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32897d853a72ffdf58e8bbc7aa5fd895e56aa5eabfab6dc6655a60ad30213386`  
		Last Modified: Tue, 30 Sep 2025 23:17:18 GMT  
		Size: 100.4 MB (100442427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fd40d8ee298ad9446970577996e75c23c71ee45ef65c7ea5e4fa35e521c7cc`  
		Last Modified: Tue, 30 Sep 2025 23:17:09 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bab24ed7aa6dcb2e3311b36b76d506bd6b982ac32bf3b02a323daf3ddbeec67`  
		Last Modified: Tue, 30 Sep 2025 23:17:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eaec38c32b136b1aef27014891cb31a728daf953d14ae4ad3060c67782f09c2`  
		Last Modified: Tue, 30 Sep 2025 23:17:09 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8356a777ad6b4ff40d60049de683a84f8d1885fcd55e138aa115d8323e777afa`  
		Last Modified: Tue, 30 Sep 2025 23:17:09 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421ac9f127e7716a8f4efb005ec91073e928bdc3a7fed822dd8a23af7303d9f2`  
		Last Modified: Tue, 30 Sep 2025 23:17:09 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:bc8d7a8efcd7d581de6f3e4487942da3069855bacba78db9d2838ff478aa8e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.9 KB (637911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c8c4dbb9b63d0d13d584078eb8a6600ef113d9e5408e0bf622f6dd32f998a3`

```dockerfile
```

-	Layers:
	-	`sha256:5430f2080b1db5118ef1e9d913824558847291e1286a8da48217b65c0302c661`  
		Last Modified: Wed, 01 Oct 2025 20:07:58 GMT  
		Size: 593.9 KB (593858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00302dd1e6c0669edebf23b5ad2cadaff47b41e6ac6d769ef071b99f1017a39e`  
		Last Modified: Wed, 01 Oct 2025 20:07:59 GMT  
		Size: 44.1 KB (44053 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine` - linux; 386

```console
$ docker pull postgres@sha256:e5de8aa389f04b703e9160e4c998bf6befa71fe357b27bed1eae5e26e38ba97e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115193981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74949bf0b135f9008395be5f839fcbb85aa791539b5c175b40ee49d5a2eb3524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV LANG=en_US.utf8
# Tue, 23 Sep 2025 19:31:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_MAJOR=13
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_VERSION=13.22
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Tue, 23 Sep 2025 19:31:05 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 23 Sep 2025 19:31:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:31:05 GMT
STOPSIGNAL SIGINT
# Tue, 23 Sep 2025 19:31:05 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 23 Sep 2025 19:31:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210bfdb77df84d165c1855ec35ee38cb9d2040804dad288722294c52f584a073`  
		Last Modified: Tue, 23 Sep 2025 21:26:54 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6363c40683dbce937640330b2a71b77001c16af2724c94c7391934889e5d2b0f`  
		Last Modified: Tue, 23 Sep 2025 21:26:54 GMT  
		Size: 886.0 KB (885977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d603a142973fbfd1eb1635b89905bba9815875261745edee936cdd814ef6d54`  
		Last Modified: Tue, 23 Sep 2025 21:35:51 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a953e1c073b81f4029c410651af3b2f6b53bbadc9f78dce47f9581c0e8f5c016`  
		Last Modified: Tue, 23 Sep 2025 21:35:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33c90710f17abc92b719956fb48e01300551d581d00534b3f991896c9fa9961`  
		Last Modified: Tue, 23 Sep 2025 21:38:27 GMT  
		Size: 110.7 MB (110676315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701fc014000abc68f825a519cbf6e38b8d7e1560e83abf489e94505dbf6d33f1`  
		Last Modified: Tue, 23 Sep 2025 21:38:18 GMT  
		Size: 9.0 KB (9013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b8a9e97f2063c5632c68b24f14a04ad01699f9f407750a2c26289ec06547da`  
		Last Modified: Tue, 23 Sep 2025 21:38:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5eb610b8860c63e00759c8e720b9b21cefe0a1d5d777e12d011e737b99321e3`  
		Last Modified: Tue, 23 Sep 2025 21:38:18 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0de32700cabc8f45ff7546fc9c5ce7b1117ef3934cd6f9fd1c43b054465308`  
		Last Modified: Tue, 23 Sep 2025 21:38:18 GMT  
		Size: 5.9 KB (5925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538955bf7b9138b36a2be3a49e58041deab40bca1c6d9c4577d7e6cf8e5ea5f6`  
		Last Modified: Tue, 23 Sep 2025 21:38:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:2b4b6800645b6e920e33ca02b78e0f8d311c33f4b5d73d094e6ab0947a34d366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.5 KB (637490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94a601c351bd748924f32512b7ffdb3d748af808566b6814455f766ae930ba8`

```dockerfile
```

-	Layers:
	-	`sha256:cafaf81f2f928360c6cb917c9d5c050c0ee7f2e355d5ef8534ea649c5567307d`  
		Last Modified: Tue, 23 Sep 2025 23:08:01 GMT  
		Size: 593.8 KB (593777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f537e5806baffa714a59dcab9e6fd46430617abd577620c15da1dcfbd40161a6`  
		Last Modified: Tue, 23 Sep 2025 23:08:06 GMT  
		Size: 43.7 KB (43713 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:dd988cf37ddf11d56f3c97e19fcd4b460ae7e1adddeb6953a556dc7b8a184677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92617247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94cb7f0e06a4aab119223bbc36b1bf1d68968d85b33f65a1bddf1300aceddafc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV LANG=en_US.utf8
# Tue, 23 Sep 2025 19:31:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_MAJOR=13
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_VERSION=13.22
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Tue, 23 Sep 2025 19:31:05 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 23 Sep 2025 19:31:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:31:05 GMT
STOPSIGNAL SIGINT
# Tue, 23 Sep 2025 19:31:05 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 23 Sep 2025 19:31:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516dda332ab75919af8404339990ac818ad4f06bee1aad9d6d4dde0c534068d0`  
		Last Modified: Tue, 23 Sep 2025 21:30:51 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed414af8e682e3ea8ea77058575e55ea0a1d7e892187e6d42ca13a35600d7986`  
		Last Modified: Tue, 23 Sep 2025 21:30:52 GMT  
		Size: 873.8 KB (873812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f732c76c2a7c14ddb4744eaa7adb07f3e9b4f1b1185c34fa88225bf6efbc7398`  
		Last Modified: Tue, 23 Sep 2025 21:55:07 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4cc69a686bf7b85825203003346674d8b30090e160ea719a54197f3e8e0b6b`  
		Last Modified: Tue, 23 Sep 2025 21:55:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a236b4ffb69a95034e284e19cf83c1a3db327c9a875bc7bbba6be511b78d1947`  
		Last Modified: Tue, 23 Sep 2025 22:41:27 GMT  
		Size: 88.0 MB (87999630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc74115efbb2d9d8f7dfa8a3e898a8d3d4eec9b7bd7052763b4c112796413a96`  
		Last Modified: Tue, 23 Sep 2025 22:41:20 GMT  
		Size: 9.0 KB (9019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b06a7ce5de6cb56f69a194cc5c834361b94e4f468a2bedb83fe67c0f2a5bc8`  
		Last Modified: Tue, 23 Sep 2025 22:41:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c3cf21d919fdea89f5d17697fcf392e83535666f5568052dcd15d3fe73232f`  
		Last Modified: Tue, 23 Sep 2025 22:41:20 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff702084956e866ce51a166ed26685c685ec644286787adbe99b600d1b83f59`  
		Last Modified: Tue, 23 Sep 2025 22:41:20 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97651b5fce78d2b137b5eeb5150b2e0a7364256a96ceac66cad0ffa1a8b9aaa`  
		Last Modified: Tue, 23 Sep 2025 22:41:20 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:7599724490849c65f46d3c977df3ae26e5c039d3b4e6845828391d9f3dc86c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.0 KB (634038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610c07bf0ae852277ced39da80f18094f2de1a076be5178f3b530e3f491e7418`

```dockerfile
```

-	Layers:
	-	`sha256:50d63df9b8acaa09868db72accadead4393bea9a7fa51845f7cc5d40ad3487cd`  
		Last Modified: Wed, 24 Sep 2025 02:07:58 GMT  
		Size: 590.2 KB (590223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7724a3ca10e969207ef9721426e06a0b7247293a13fd1c00bde9c382eb7d8360`  
		Last Modified: Wed, 24 Sep 2025 02:07:59 GMT  
		Size: 43.8 KB (43815 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:1d809c246bd9813c7f71ff1d0d8038d887c187a0da8e1b2722c38a16f0cd98b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108269831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71b50be8dfca166f23d4fb780e109fb3a19efac5c387f5ebca5361ba2643272`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV LANG=en_US.utf8
# Tue, 23 Sep 2025 19:31:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_MAJOR=13
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_VERSION=13.22
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Tue, 23 Sep 2025 19:31:05 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 23 Sep 2025 19:31:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:31:05 GMT
STOPSIGNAL SIGINT
# Tue, 23 Sep 2025 19:31:05 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 23 Sep 2025 19:31:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e619170c917844505026e149fdeddc26bba3eb3ed14275ee3d058323b20633f1`  
		Last Modified: Wed, 24 Sep 2025 03:55:05 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89fd9f84d7701f270a736645c6418f98ed6f66b25c5a32aea7002df49465eb1`  
		Last Modified: Wed, 24 Sep 2025 03:55:06 GMT  
		Size: 860.9 KB (860904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4358132b2e5c9cc1f4692234e66f72228883f0b741f8e2fa2de2357636a325f3`  
		Last Modified: Wed, 24 Sep 2025 07:56:32 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e93176d9e70ab0c66cbb82254df3b120d8f1ffa52e646d5fbe89930fb9c13e`  
		Last Modified: Wed, 24 Sep 2025 07:56:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005f8f096bb219643a4c4e9448d894fb863f8494e35899b25f39a804951a948`  
		Last Modified: Wed, 24 Sep 2025 21:51:11 GMT  
		Size: 103.9 MB (103879423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10272ac55bdcf5bca2d63683735b6a554c5f62ba3cdc2b35d3104a66a47b28d6`  
		Last Modified: Wed, 24 Sep 2025 21:51:06 GMT  
		Size: 9.0 KB (9023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf8a2bcb0dc3d6f38de72b13ee1b3b182ed5ef890be070f48b6ab3623f85092`  
		Last Modified: Wed, 24 Sep 2025 21:51:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2babc308d311883c91674a46c8b0b55c1f4bbce934c0af8787afcd3b6fa9f7f`  
		Last Modified: Wed, 24 Sep 2025 21:51:05 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67c7e39a9ca07cb4d4e2aac5b5e757950af3a70432323608d17fe8fb1ee65a3`  
		Last Modified: Wed, 24 Sep 2025 21:51:05 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42afe7085955eb27daf10ce03fb5d15409c429cb0efdb389816e3469a8e64797`  
		Last Modified: Wed, 24 Sep 2025 21:51:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:8dd6c6b60f857740a266c3fbcf89bc6690f67f07a88d471687facd301522d310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.7 KB (635702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae1c2229bc315402180d040db8b8d7d147723a18ba160daf4b483410d3e04b2`

```dockerfile
```

-	Layers:
	-	`sha256:4215d26560e6b39a08a0245fc2a82f8384f2a78440e1559051fb997c71e03195`  
		Last Modified: Thu, 25 Sep 2025 02:07:23 GMT  
		Size: 591.9 KB (591881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c9c190cb275bed2699d8441d85e56c7955bf81d84f3d70f4d0419c2955f2f81`  
		Last Modified: Thu, 25 Sep 2025 02:07:33 GMT  
		Size: 43.8 KB (43821 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:bec8d6237ee3ea94a157e89152220edc1f24e00c6fbe50239279be6a15d18f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117528904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd2da1c3de1694c34ddfff7fa85474cdbe4aa4aba937b6f486f836cb06f32fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
ENV PG_MAJOR=13
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=13.22
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b61fd0cd054cbd267edfc4e0f9ea6ca2d4ea99df522313b0eed8407c94db55`  
		Last Modified: Tue, 23 Sep 2025 21:55:55 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6141a601d228a980604c34f10ef78a424142e0b3df3599efbb2d2a87c6f63a94`  
		Last Modified: Wed, 01 Oct 2025 04:46:07 GMT  
		Size: 891.3 KB (891274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c7d0abd8042672d0518d19b8e0485bcf821df484d9ccba4a21e0381edc104c`  
		Last Modified: Wed, 01 Oct 2025 05:04:03 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b146c42f008a195d853d9a586b6d76d87c679acb2f81c3d83d440631281d00`  
		Last Modified: Wed, 01 Oct 2025 05:04:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0612100c4290ff68e19891004af52c61def0a255b7b0dd7665c567c0d360eafc`  
		Last Modified: Wed, 01 Oct 2025 05:28:37 GMT  
		Size: 113.0 MB (112975968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771a3c0a600aff05df7039610c958f0a581818332ef0addde488929867f63fb5`  
		Last Modified: Wed, 01 Oct 2025 05:28:28 GMT  
		Size: 9.0 KB (9021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e645707e4f7c0bb0ac272546825b06fa810157e74d740b85151b744fde4ea5c`  
		Last Modified: Wed, 01 Oct 2025 05:28:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511c05f6dd3dcb04f972e54eb5b364d78485ab6f011003b681ced007ad7614c8`  
		Last Modified: Wed, 01 Oct 2025 05:28:30 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877b55c113434bd2e474f242e52ea0ef2996fcbd50e3953f6534150562906374`  
		Last Modified: Wed, 01 Oct 2025 05:28:30 GMT  
		Size: 5.9 KB (5925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e694e8281d1c43bbdcd0d1fa808d5a1b4bfe9a0efe3a981f71eef9d3d92ef54`  
		Last Modified: Wed, 01 Oct 2025 05:28:31 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:85a897a01452de3bb887cd916d3aeed6f3a82c94bf4b25c260563c43f95fbdb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.7 KB (635680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f618365525261ee6506bea3cd75dfbd29b2a031b3ae9adda7b12d8032bcebb5`

```dockerfile
```

-	Layers:
	-	`sha256:b5969402519ee2db8d5df8874546cc8269b3489d8d8b7787fbdd07f1b89d0d40`  
		Last Modified: Wed, 01 Oct 2025 20:08:09 GMT  
		Size: 591.9 KB (591851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5fa12218e838b31530a8288c2997af9ffce563035ed8a5384340880779345d7`  
		Last Modified: Wed, 01 Oct 2025 20:08:10 GMT  
		Size: 43.8 KB (43829 bytes)  
		MIME: application/vnd.in-toto+json
