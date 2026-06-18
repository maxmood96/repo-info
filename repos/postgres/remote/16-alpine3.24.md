## `postgres:16-alpine3.24`

```console
$ docker pull postgres@sha256:e013e867e712fec275706a6c51c966f0bb0c93cfa8f51000f85a15f9865a28cb
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

### `postgres:16-alpine3.24` - linux; amd64

```console
$ docker pull postgres@sha256:0fc5c901ec0a3c55ce70b99b040daeb89d5b35b61febbced1b4b24dbc3153ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116016918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e684c11a6c7c127c1b7602063cc6a13db0a12b62dfd770d83936c089751d498d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:58:29 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:58:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:58:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:58:31 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 16 Jun 2026 22:58:31 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:58:31 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:58:31 GMT
ENV PG_MAJOR=16
# Tue, 16 Jun 2026 22:58:31 GMT
ENV PG_VERSION=16.14
# Tue, 16 Jun 2026 22:58:31 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Tue, 16 Jun 2026 22:58:31 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:00:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:00:46 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:00:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:46 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:46 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2eaa02a04a98fb1212dabec618e3ca73901e1ad25004bc164108b707c18ff0`  
		Last Modified: Tue, 16 Jun 2026 23:01:02 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4fedf9cad8bcf4f644fa6801e08e1772f7571abb28ae7299d4471911a8632c`  
		Last Modified: Tue, 16 Jun 2026 23:01:03 GMT  
		Size: 900.3 KB (900253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f6aac6fe130aaf8e6c7ea279af3b5d3959d23f93da231f471bd8384c38ad19`  
		Last Modified: Tue, 16 Jun 2026 23:01:02 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2511ae13411ce16418b840e0a454e1e0846c78cd34bd965565aca9a49621000`  
		Last Modified: Tue, 16 Jun 2026 23:01:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63c7a8df82b7afa52f17cfd21453855ce8855d0f34e17148cd3522d76ff6c21`  
		Last Modified: Tue, 16 Jun 2026 23:01:07 GMT  
		Size: 111.3 MB (111252815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbe267206710f0f3126c9f5463fc7ae0862a125a6483fa36e1b0a38bd9b6650`  
		Last Modified: Tue, 16 Jun 2026 23:01:04 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddab922e8d89ffe4bc99df343586b06c82bd7bfca396ed2a418731d966dbfebe`  
		Last Modified: Tue, 16 Jun 2026 23:01:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e4c51fed832f64e1cc735d59aa7f38fc1ac00d52aca174220f38ee1bc176a0`  
		Last Modified: Tue, 16 Jun 2026 23:01:06 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de95df2a1fbb47881bbdb9c9b1e9d5fbb6c1b2577a14d2bb16c9b57aee78a75`  
		Last Modified: Tue, 16 Jun 2026 23:01:05 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84bc3f3ded66f4af523e5346f290a3c421d3f83e791b3f4877af02fd3065708`  
		Last Modified: Tue, 16 Jun 2026 23:01:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:7640730507814032f78f54f10345e7991e6dfadef294babca133f053b5c0bd77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.3 KB (642340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb392cfb6c05a25f2c2d6ebb72b128dd5ea8c73f308572c43403047d35e4ff0`

```dockerfile
```

-	Layers:
	-	`sha256:bf118c795fb84a1315321f5ae1d75e6c9dbe0b9404974310f73dd2492e978c2f`  
		Last Modified: Tue, 16 Jun 2026 23:01:05 GMT  
		Size: 598.0 KB (598034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fa7d9e114673ed211c440ae85c561e89ef294b6b12d129d410063df55f709a`  
		Last Modified: Tue, 16 Jun 2026 23:01:03 GMT  
		Size: 44.3 KB (44306 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.24` - linux; arm variant v6

```console
$ docker pull postgres@sha256:ddcdcf3beaea17030cd504554957d33a29d7a45930689bded84f20609331c372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112256820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273ec506e79fc8fbaf91cf54f45cd091a4b8ac3cc2daf0f95cccf45aaae6a621`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:57:27 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:57:30 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:57:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:01:06 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 16 Jun 2026 23:01:06 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 23:01:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 23:01:06 GMT
ENV PG_MAJOR=16
# Tue, 16 Jun 2026 23:01:06 GMT
ENV PG_VERSION=16.14
# Tue, 16 Jun 2026 23:01:06 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Tue, 16 Jun 2026 23:01:06 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:04:04 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:04:04 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:04:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:04:04 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:04:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:04:04 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:04:04 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:04:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:04:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:04:05 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:04:05 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:04:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25018f469fafccf804bf9e783ac48f87c1aec0163bd1119c1a6166dac72e3cc1`  
		Last Modified: Tue, 16 Jun 2026 23:00:44 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dbe011944959749e7f5f74ee647a20e3ea9acdb3178cb9059af359c3a45af6`  
		Last Modified: Tue, 16 Jun 2026 23:00:44 GMT  
		Size: 864.6 KB (864612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aa642547e91d8c49615588426657501d4fa306fc876ee0db3e5d60f7a2ceb4`  
		Last Modified: Tue, 16 Jun 2026 23:04:16 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f60a2871bc4fe03001c2402dc4158dbb2ad40f9fa629af3f2ee1e54127d2c15`  
		Last Modified: Tue, 16 Jun 2026 23:04:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3498dc5a3d354db198ed31e21c6ad865e7bb0c6e95c2e2db821b8116b0dfd0`  
		Last Modified: Tue, 16 Jun 2026 23:04:20 GMT  
		Size: 107.8 MB (107821300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb47bbd1cd14ac63721124508ba95f3f3d534e5ef67ff7ab06048debbb684a5e`  
		Last Modified: Tue, 16 Jun 2026 23:04:16 GMT  
		Size: 9.6 KB (9617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2320e1b5fdd49f6318fb72aca75c7d45604ee464533d7b06fd528f5aa9af91ec`  
		Last Modified: Tue, 16 Jun 2026 23:04:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1388d957383de00cb3a47839fd954d1a351a07d5ca13f8c106c64d4c4a965b26`  
		Last Modified: Tue, 16 Jun 2026 23:04:18 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782981bc601d0608fda3726d50f99beaabc78563248bec0981e20b2ae49fc911`  
		Last Modified: Tue, 16 Jun 2026 23:04:18 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6288e5ed53efdd6750dfa27c72d9f4b2bd9870372fc254a81212d5fad1cbb49b`  
		Last Modified: Tue, 16 Jun 2026 23:04:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:99cd59dfa579fb9f4cd7a98f892763dfc70aeb615b8be5a319e79012de6723d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 KB (44275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b9627c13d642b6811d5ce060a290600a8ae0a2c56d3a9b79e7bf25aa5c5916`

```dockerfile
```

-	Layers:
	-	`sha256:2fd257003c97473449f0a6c764cf68e90b7c7afb1f28d6e83cb781ff83e8438d`  
		Last Modified: Tue, 16 Jun 2026 23:04:16 GMT  
		Size: 44.3 KB (44275 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.24` - linux; arm variant v7

```console
$ docker pull postgres@sha256:ddf1452376d3455f11a40993b5ca003ce1661c6900164edd2346704f0093b2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (105967833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7cf4eff555a4913735a35f62e64847561135808826f095eeac3a223d3dc915`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:57:36 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:57:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:57:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:01:01 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 16 Jun 2026 23:01:01 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 23:01:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 23:01:02 GMT
ENV PG_MAJOR=16
# Tue, 16 Jun 2026 23:01:02 GMT
ENV PG_VERSION=16.14
# Tue, 16 Jun 2026 23:01:02 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Tue, 16 Jun 2026 23:01:02 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:03:53 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:03:53 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:03:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:03:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:03:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:03:53 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:03:53 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:03:53 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:03:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:03:53 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:03:53 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:03:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d30475b80f928512747a8ce9adc0b4ad9229130244f3b258cd34083ab8ec30`  
		Last Modified: Tue, 16 Jun 2026 23:00:44 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e94f569ab76e4c75076374599f74e1340c0d3b9601ae8beace7d3fd05558750`  
		Last Modified: Tue, 16 Jun 2026 23:00:45 GMT  
		Size: 864.6 KB (864634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9133cffe4c54d9ee50e59b454f98f2fcda04c29e0107db9d579b466f76dcc05b`  
		Last Modified: Tue, 16 Jun 2026 23:04:07 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e7ab207913660af6b1d2b389f2d4977cc66ddb2ead85cf35d2f7613eb33f48`  
		Last Modified: Tue, 16 Jun 2026 23:04:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb9d26a201e039e833e7639e94367bc86a7fda8170a04305bb73e0922a742ff`  
		Last Modified: Tue, 16 Jun 2026 23:04:10 GMT  
		Size: 101.8 MB (101825129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd6d3d9024a321a71b9a1e6812e2e252231c23c5a119f281aad8957edf1cd45`  
		Last Modified: Tue, 16 Jun 2026 23:04:07 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df6684c8f1edef1f301c12ab5ee448ad8ea17f6d50af5842edd35f755640780`  
		Last Modified: Tue, 16 Jun 2026 23:04:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4faee2db772a250aa94f394919e639d375915d6d6fbf4416a72face2bc3c9ac`  
		Last Modified: Tue, 16 Jun 2026 23:04:09 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074c53c03541c5ce93eb792ca66e385d3289303e55b0d17ac9b08bf9cf18cc52`  
		Last Modified: Tue, 16 Jun 2026 23:04:09 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3f7034503aa84e572e99a9530d84a42ed0643fcda5ce330e6cd6346325cc70`  
		Last Modified: Tue, 16 Jun 2026 23:04:10 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:42bc91b254d41a5772e3952778e9f89973c9ffbd0140f88a96a39df483d77fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.9 KB (641910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963181260a36f552b16456cc4c2e897d383666fa559a26cd3c1c19dbd6cbf64a`

```dockerfile
```

-	Layers:
	-	`sha256:b97c859bc5015e30e0547206ad17dba562d0c802d2710ea140c17dba526dcd51`  
		Last Modified: Tue, 16 Jun 2026 23:04:07 GMT  
		Size: 597.4 KB (597420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b56ec7564d022f12d33f9f4a5845847002bce07e3eb9b79184e6ff87f1e3e71c`  
		Last Modified: Tue, 16 Jun 2026 23:04:07 GMT  
		Size: 44.5 KB (44490 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:a43e7e01a2fe7e9ce2b6ecc02dbe2ef27089958e2edff8d6a0b64f86a9b2c243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113847689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab885cf71916beded83c51df1ea71acddeab24048fd957b4f4471f59dcb9bc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:58:29 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:58:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:58:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:58:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 16 Jun 2026 22:58:32 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:58:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:58:32 GMT
ENV PG_MAJOR=16
# Tue, 16 Jun 2026 22:58:32 GMT
ENV PG_VERSION=16.14
# Tue, 16 Jun 2026 22:58:32 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Tue, 16 Jun 2026 22:58:32 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:45 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:45 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:45 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:00:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:00:45 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:00:45 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:46 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:46 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d0fadf898a968f51145417e2318994b5bc8a836f944142bebe8cf6c64fe4e3`  
		Last Modified: Tue, 16 Jun 2026 23:01:02 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce425ecfaaa3b69e6663f7ba31ee679c24743420c736873d0bc5915cdea9b40`  
		Last Modified: Tue, 16 Jun 2026 23:01:02 GMT  
		Size: 852.3 KB (852267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6498537e6761807bb9e7ff2d7f98d797f5789578788e7437c6ee19d7f3bbb23e`  
		Last Modified: Tue, 16 Jun 2026 23:01:02 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cc3e839ffda2890a7b287da7025adf05ce89b13c8ff87bae69b56d89927f44`  
		Last Modified: Tue, 16 Jun 2026 23:01:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e3aee4221bd9f12d8d9bdae19e584a0f7d11a3422f64b2f0b6022952b28541`  
		Last Modified: Tue, 16 Jun 2026 23:01:06 GMT  
		Size: 108.8 MB (108794925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d052215e28f35280f45abe1302b553b705f083c89a89e6a20b735d4ebd776303`  
		Last Modified: Tue, 16 Jun 2026 23:01:03 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3865b2f387acd1f28cada9e946146f40f3fcd0b53c8b88803920b07bbda858`  
		Last Modified: Tue, 16 Jun 2026 23:01:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9e69e30b63c0edc92f33409e14afaec96f417888f7a29be397f27697fcfda4`  
		Last Modified: Tue, 16 Jun 2026 23:01:07 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f56633e156ad6d971a610a9b2a0222e4182791cbdf305b42895d481ba0ab997`  
		Last Modified: Tue, 16 Jun 2026 23:01:08 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff0b682b155e7a7623557b27d8ba5c889fda904cad059a5a907aca1a7884847`  
		Last Modified: Tue, 16 Jun 2026 23:01:09 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:d88bd9acd62f3487f78c2439464b96404e30c763b623ce1c6db4e2c0acaca14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.0 KB (641970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04995ea85b63126691e9582ed7ec43b402f94fbe03de9a30fe61a365fbc274d`

```dockerfile
```

-	Layers:
	-	`sha256:448e59628ba688e542c3a797ad33bdfc96baad829f829a18cd46aac43e8570f8`  
		Last Modified: Tue, 16 Jun 2026 23:01:02 GMT  
		Size: 597.4 KB (597440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:219b887dc3ef0feab47fe67dddbd0dc3862a3868066233ff4298c5e3651fa44b`  
		Last Modified: Tue, 16 Jun 2026 23:01:02 GMT  
		Size: 44.5 KB (44530 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.24` - linux; 386

```console
$ docker pull postgres@sha256:e6db27d2e13ff29fb5dd9f34cd7c377901d008c23c9b68c853ec0a538e0b6e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122676290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:315fd961edb6e64e1cdfd2c6bcfa8599a7eab190a73b2e10fcfae3d3ff354970`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:58:54 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:58:57 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:58:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:58:57 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 16 Jun 2026 22:58:57 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:58:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:58:57 GMT
ENV PG_MAJOR=16
# Tue, 16 Jun 2026 22:58:57 GMT
ENV PG_VERSION=16.14
# Tue, 16 Jun 2026 22:58:57 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Tue, 16 Jun 2026 22:58:57 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:01:32 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:01:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:01:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:01:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:01:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:01:32 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:01:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:01:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:01:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:01:32 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:01:32 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:01:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675fbd767b5d9beff2a82fb0b0ef73c90b1cd39b8804664115c0c283fb2452dc`  
		Last Modified: Tue, 16 Jun 2026 23:01:48 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54832f5633e6a8beb56b0539ea9b560f34cecc0d21ec6015e8bba9ea2c5dc913`  
		Last Modified: Tue, 16 Jun 2026 23:01:49 GMT  
		Size: 868.4 KB (868431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd4f3d85eb67acb8cd873f0c1634b5cf87f0b7fff764da2d323f74c38969ad1`  
		Last Modified: Tue, 16 Jun 2026 23:01:48 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2721d669c8ffca5f339ae5821c9b230a9f91d472d69e937a8c50f15cd2eeb7db`  
		Last Modified: Tue, 16 Jun 2026 23:01:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0511e3fedf78d5644e50f10a04ce09b8ffa8eb7f639b59b5ecf4af12b6e7693c`  
		Last Modified: Tue, 16 Jun 2026 23:01:52 GMT  
		Size: 118.1 MB (118120260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be18ff391690707b08f934edc4de0d8ac5d8896009df1c3c1187e52b2c81237b`  
		Last Modified: Tue, 16 Jun 2026 23:01:50 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6134349300da5780e855c1f651d40074d26a31132c68631e41ace4f8a4eabb3c`  
		Last Modified: Tue, 16 Jun 2026 23:01:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44d15d2581cc39e75618ca70abb4e3256e79be2722da8be5015f62068efb3b8`  
		Last Modified: Tue, 16 Jun 2026 23:01:50 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06225d8bac7a4a52735d899a4b0c1ceb4ed19ad7ed87a9b504fd535201ffebf1`  
		Last Modified: Tue, 16 Jun 2026 23:01:51 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8859123bb8459e82de84da0e7ef275862df106a3524c684817dd54681aa0c8`  
		Last Modified: Tue, 16 Jun 2026 23:01:51 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:1c208a0851b81fd430984c4a9e7a154d993eec222e608b5e71c04026886bc126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.3 KB (642266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1847fb228765391fb4c5ecc48bc2bd52e08ec3b2b7a89eab003d2294184ddb2`

```dockerfile
```

-	Layers:
	-	`sha256:08f9a0faed78c5b00d759a147fc01d52f27477b293111f56b238fa894a2747ef`  
		Last Modified: Tue, 16 Jun 2026 23:01:49 GMT  
		Size: 598.0 KB (598009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f9aed29ce4461072e8222bfed06a9ccafd043b8ae118e027acd2719e56138ba`  
		Last Modified: Tue, 16 Jun 2026 23:01:49 GMT  
		Size: 44.3 KB (44257 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.24` - linux; ppc64le

```console
$ docker pull postgres@sha256:4927c0ef74e19fefd6b23ff36023217d727eac29837a6cb039d74a4936c52b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118706740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03de430b99e66ff5021184089ca007c508334e6f682f9b28bff446b779f3b750`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:56:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:56:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:56:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:12:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 16 Jun 2026 23:12:14 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 23:12:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 23:12:14 GMT
ENV PG_MAJOR=16
# Tue, 16 Jun 2026 23:12:14 GMT
ENV PG_VERSION=16.14
# Tue, 16 Jun 2026 23:12:14 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Tue, 16 Jun 2026 23:12:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:16:21 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:16:21 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:16:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:16:22 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:16:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:16:24 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:16:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:16:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:16:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:16:25 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:16:25 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:16:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a550c138b135a89330347b3a13776cce136b1e19d05c3e2b10571ce2135769`  
		Last Modified: Tue, 16 Jun 2026 23:01:22 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86fd92e78cd7b0d10ecc0f0da5decbed7534334b833b91ed30473a9d6fcb1f`  
		Last Modified: Tue, 16 Jun 2026 23:01:22 GMT  
		Size: 857.4 KB (857445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664dfe9e7b8ba874c43b4eae9ed442df98264c6d9336e53b927c836a044de4e0`  
		Last Modified: Tue, 16 Jun 2026 23:17:01 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b334be2a72215ddf0813fb1a98ca70d172379ae40f730d5c2195ba55291ef56b`  
		Last Modified: Tue, 16 Jun 2026 23:17:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953ac45480f70de5fc641282b8519fc306ef5facfa8c0b1d59ba2bbda04c163c`  
		Last Modified: Tue, 16 Jun 2026 23:17:05 GMT  
		Size: 114.0 MB (114018416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19768d950846ccf14cb6987ad3cd15003f10c82de49f4e485e3d82aa74f50484`  
		Last Modified: Tue, 16 Jun 2026 23:17:01 GMT  
		Size: 9.6 KB (9629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e5de0d4257fe63cde2ceaf4e8248b1220a46e13a622069a633cf79474efd3c`  
		Last Modified: Tue, 16 Jun 2026 23:17:03 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc369abada48439430c2313e400f3ab42315bea9041e5456a996ffd222ffc741`  
		Last Modified: Tue, 16 Jun 2026 23:17:03 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e413e29b22ced7011f0afe243131ab522c62a286371cf4cb30369a5f972ca6`  
		Last Modified: Tue, 16 Jun 2026 23:17:03 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530218b1075e17fcbde5a9998899a07cabfa554421c407db4db021399397a749`  
		Last Modified: Tue, 16 Jun 2026 23:17:04 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:77732375a17f3eb80cbfff6036e0ebad45c7a439cc492c31c36e41e488560130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.1 KB (640121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f423c1b4c8bd9c0f573f477f33349950a04d5bdd91b613e1433d5feeadba453d`

```dockerfile
```

-	Layers:
	-	`sha256:60869934e81939eecd2e62a5acb0efe93856538811da4af1937710b7413a3d34`  
		Last Modified: Tue, 16 Jun 2026 23:17:01 GMT  
		Size: 595.8 KB (595755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dee15fc5396ded52130cd8286f532eee3c13133d82e67e384662083b9a1198df`  
		Last Modified: Tue, 16 Jun 2026 23:17:01 GMT  
		Size: 44.4 KB (44366 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.24` - linux; riscv64

```console
$ docker pull postgres@sha256:f1d4acf302f9d44f45d9a85ac14cf06d27449f501732960a90f9f7a9c8ab2ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118104800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12583d7b4380cbdd5a662d5a2613b01ef2eddd2593c0833ed8967760b5233460`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Wed, 17 Jun 2026 20:22:02 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 17 Jun 2026 20:22:13 GMT
ENV GOSU_VERSION=1.19
# Wed, 17 Jun 2026 20:22:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 02:07:29 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 18 Jun 2026 02:07:29 GMT
ENV LANG=en_US.utf8
# Thu, 18 Jun 2026 02:07:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Jun 2026 02:07:29 GMT
ENV PG_MAJOR=16
# Thu, 18 Jun 2026 02:07:29 GMT
ENV PG_VERSION=16.14
# Thu, 18 Jun 2026 02:07:29 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Thu, 18 Jun 2026 02:07:29 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Thu, 18 Jun 2026 02:59:45 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Jun 2026 02:59:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Jun 2026 02:59:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Jun 2026 02:59:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Jun 2026 02:59:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 18 Jun 2026 02:59:47 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Jun 2026 02:59:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 02:59:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Jun 2026 02:59:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 02:59:47 GMT
STOPSIGNAL SIGINT
# Thu, 18 Jun 2026 02:59:47 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Jun 2026 02:59:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63bc382ee77772838b6762efb5dc9918aac46cc99c959111411a578a706e8e9`  
		Last Modified: Wed, 17 Jun 2026 21:18:05 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac745ca8a6a40fa8931eea62c6eada5afee35c1c91aede732f42ba0aba848664`  
		Last Modified: Wed, 17 Jun 2026 21:18:05 GMT  
		Size: 844.9 KB (844939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04af9fb0c1657dde4ed06cad73e1f6f1f88358f9c40e7b29d9a9811383c526f0`  
		Last Modified: Thu, 18 Jun 2026 03:02:44 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6162e785d2f8fd62f901324e82906cc4940fd02456304143ec1c4fd9f62f07`  
		Last Modified: Thu, 18 Jun 2026 03:02:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd90fccb326262a4cf130c412caf7f969fa953e75c6dcf199e7de1dfaf388c7`  
		Last Modified: Thu, 18 Jun 2026 03:03:01 GMT  
		Size: 113.7 MB (113668023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968a288bbfa06a8e293868abc99001568f68b556e83d82a8ab33264619341628`  
		Last Modified: Thu, 18 Jun 2026 03:02:44 GMT  
		Size: 9.6 KB (9631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550f77023fa5b2f6f580098a7af5d74364b34798f0ed8c2f7520173a9709ffc3`  
		Last Modified: Thu, 18 Jun 2026 03:02:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448865172079dfc3aaf2e0a399f0c9178e88fadb4c460729ccf633bb3cea522c`  
		Last Modified: Thu, 18 Jun 2026 03:02:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8497619fd0bed2ecf4ffbb88ab460ebbe18ebe41ea2d61e869faa9d44628cda`  
		Last Modified: Thu, 18 Jun 2026 03:02:46 GMT  
		Size: 6.1 KB (6102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eaff7446226db4ad784521abf66db7524f4890b599c9a68c548527a5361b087`  
		Last Modified: Thu, 18 Jun 2026 03:02:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:2ada1479dcef761bc65d26c16da75cf17bf84550c15bd3171a271ab7c1262604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.8 KB (641779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb30b37b8b2f74aa1a6f7e81103c316bc78aa5165f9b908e1bf8cbe76abd7951`

```dockerfile
```

-	Layers:
	-	`sha256:862ae1b78f67b7981be9fb32aad3fe764f01499fbc847323904b3d6db39d89c6`  
		Last Modified: Thu, 18 Jun 2026 03:02:45 GMT  
		Size: 597.4 KB (597413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3767a8cd495ae7e3caf54efee76093eca7d4b6a502af24d8dd0f6c87250c10d9`  
		Last Modified: Thu, 18 Jun 2026 03:02:44 GMT  
		Size: 44.4 KB (44366 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.24` - linux; s390x

```console
$ docker pull postgres@sha256:4fc366518c44948b7e88657bc69e7676736cf195039c967889973875990a4601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122525412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc66bcf30944f647f6a557a7fc25d5064fece1fa78a8bc67d4fa5e79100dad11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:56:31 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:56:34 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:56:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:02:05 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 16 Jun 2026 23:02:05 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 23:02:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 23:02:05 GMT
ENV PG_MAJOR=16
# Tue, 16 Jun 2026 23:02:05 GMT
ENV PG_VERSION=16.14
# Tue, 16 Jun 2026 23:02:05 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Tue, 16 Jun 2026 23:02:05 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:06:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:06:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:06:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:06:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:06:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:06:30 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:06:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:06:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:06:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:06:30 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:06:30 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:06:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52132c4d8fde8082c15540b29256e2360f2c6de68191ad0e46bc71ec74cdc17f`  
		Last Modified: Tue, 16 Jun 2026 23:01:43 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abc6a5451d4cc8391999b7fe99a4a79df7ab9b3d307f2f9e012ae4ea28dfb70`  
		Last Modified: Tue, 16 Jun 2026 23:01:43 GMT  
		Size: 874.5 KB (874490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0731dcf5cb2d8b3c5ed62f929b7b76fb4b1869f59ae839f8acbc53f3d0ca44`  
		Last Modified: Tue, 16 Jun 2026 23:06:56 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c5dd37845c73dafd37443171cc6c2df467255dc46daa591bd1c37afbb9b189`  
		Last Modified: Tue, 16 Jun 2026 23:06:56 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b4da8d486e7dcc706565c8851229b49274a136418b8983ad8768edede57c4e`  
		Last Modified: Tue, 16 Jun 2026 23:06:58 GMT  
		Size: 117.9 MB (117924141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323ba1fa738fcb51377ef2cd123789c669320928b4e8889c730a1d29a1f8f9d9`  
		Last Modified: Tue, 16 Jun 2026 23:06:56 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e74b1e89d3a2ee7256505fe08e2e1987d79a056e08cfbab8be0ba4c26612814`  
		Last Modified: Tue, 16 Jun 2026 23:06:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13332b02ab3c25ecb93ba63fdf3dd1c82b37a5340ae0bff53e59c4990cc9ea7`  
		Last Modified: Tue, 16 Jun 2026 23:06:57 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fc3f3d6dcae5d46dcca697652d5ab2bdda98703c5bb93af91fd5f4207f3859`  
		Last Modified: Tue, 16 Jun 2026 23:06:57 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c12f57d492d0d6a6af977a41983a35a62b9950f030c4b167599173b7dfd4f7`  
		Last Modified: Tue, 16 Jun 2026 23:06:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:0fae5aba67c07a1f1c9cf427842dd081b22d10409eac807948a4db77bbcdd789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.7 KB (641689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8589b4313946cc03a6be3a1980d5ef7a79d7c4ef4459553c57c549f85658a6`

```dockerfile
```

-	Layers:
	-	`sha256:37c205fa85f773f9e965d0eedf20832c08b58eb32ead9e30d9e7b681c417b579`  
		Last Modified: Tue, 16 Jun 2026 23:06:56 GMT  
		Size: 597.4 KB (597383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4acc1ca4f832d530abc8d2dbfb56a63a9952c588e75e5f3c1d1de00d1eee428d`  
		Last Modified: Tue, 16 Jun 2026 23:06:56 GMT  
		Size: 44.3 KB (44306 bytes)  
		MIME: application/vnd.in-toto+json
