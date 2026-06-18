## `postgres:16-alpine3.23`

```console
$ docker pull postgres@sha256:aed434cd14d474ee8afb77785c752ce692fee2b35541778a4d5323cf1fc7dcde
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

### `postgres:16-alpine3.23` - linux; amd64

```console
$ docker pull postgres@sha256:33a7185fbc35ba92e535144dac47310df77a868d161c186064816bab8c85146a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 MB (118027191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f20eb183be5a050ba1ec7649436068a1ce25bfd59e7f2554086fc27b55ae14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:58:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:58:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:58:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:58:50 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 16 Jun 2026 22:58:50 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:58:50 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:58:50 GMT
ENV PG_MAJOR=16
# Tue, 16 Jun 2026 22:58:50 GMT
ENV PG_VERSION=16.14
# Tue, 16 Jun 2026 22:58:50 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Tue, 16 Jun 2026 22:58:50 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:01:07 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:01:07 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:01:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:01:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:01:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:01:08 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:01:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:01:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:01:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:01:08 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:01:08 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:01:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997a662224105e6c62615203728e188d2951748ca26c1ab64f7b6f38ec8ceab8`  
		Last Modified: Tue, 16 Jun 2026 23:01:26 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50be4b6af5e50abe00f494372bf68136bfa5f1b8acaa042c259021c3088e1ce0`  
		Last Modified: Tue, 16 Jun 2026 23:01:25 GMT  
		Size: 919.1 KB (919053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf48f1442c00f47d57dcd8555d716679757d358a40e45d3daf8179a33af37f2`  
		Last Modified: Tue, 16 Jun 2026 23:01:25 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328ce21f1faf65920cb22bb010ca16889be5be97b6d17870fc3e16a52f19f3a`  
		Last Modified: Tue, 16 Jun 2026 23:01:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4758417d3301a5d02749cfa33496dbca2fe19eb1d1cd08874416b319ec4d2d6`  
		Last Modified: Tue, 16 Jun 2026 23:01:29 GMT  
		Size: 113.2 MB (113226489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044987b92b168ffe0f6baf0e961a3098e029344de5835642870e4e5715f51312`  
		Last Modified: Tue, 16 Jun 2026 23:01:26 GMT  
		Size: 9.6 KB (9618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f77fd5d08c50018daec566202523d9da5863bc426c6b76a548dbdf819e0b402`  
		Last Modified: Tue, 16 Jun 2026 23:01:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36821617346de797f0c232d8d5a72f3b55e0ae82c9323f39a76bf7502fd1f15c`  
		Last Modified: Tue, 16 Jun 2026 23:01:28 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a5916bdbfeef98405ef978d7cb4d50b33a075db6a2fdc5b5a0afd82af05074`  
		Last Modified: Tue, 16 Jun 2026 23:01:29 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822e0a23e40f5ddc5ca0c5b15d7522cc4456bee1d791dc995d1d8034117224ee`  
		Last Modified: Tue, 16 Jun 2026 23:01:29 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:1e9f3cc55af7edafecdc240b3621d16d3fbf15b2c30187e68f23e95ada82ef41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.1 KB (641142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97ebc6c9aff3f429e3d0068819eaec0eef4905fb1f926f0da6ad79d3aa439f0`

```dockerfile
```

-	Layers:
	-	`sha256:3daf1aa55a3b82a5cf69b54187aeb000e38702acaa4212adf3585e0c140439be`  
		Last Modified: Tue, 16 Jun 2026 23:01:25 GMT  
		Size: 597.5 KB (597458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33e0bc738a8a085c2ac59b1a6052b5c9c72f698d8d3c7e231ae611ddc4237ac8`  
		Last Modified: Tue, 16 Jun 2026 23:01:27 GMT  
		Size: 43.7 KB (43684 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; arm variant v6

```console
$ docker pull postgres@sha256:fccfb835a1c0b53138e387bc4f23628e014eb057a7f26b7676049cf5d1ee147f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113911244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a1951144c638b07bb512c10db9d62589e8797ca1aaa025e0db27ca16d13337a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:57:58 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:58:02 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:58:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:01:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 16 Jun 2026 23:01:14 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 23:01:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 23:01:14 GMT
ENV PG_MAJOR=16
# Tue, 16 Jun 2026 23:01:14 GMT
ENV PG_VERSION=16.14
# Tue, 16 Jun 2026 23:01:14 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Tue, 16 Jun 2026 23:01:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:04:10 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:04:10 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:04:10 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:04:10 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:04:10 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:04:10 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:04:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:04:10 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:04:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:04:10 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:04:10 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:04:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd59d2f0dcf84650ba722cc0f3d18f1b89b27985b389ae5c2a83b5d35e308c19`  
		Last Modified: Tue, 16 Jun 2026 23:01:04 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955cbba7221c3dab216cd282da7a5c3e7c080472ab30469c4acc2039d7ea92c7`  
		Last Modified: Tue, 16 Jun 2026 23:01:04 GMT  
		Size: 887.1 KB (887125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badfdc7c65660837fd76de247356d2daa993f3222f9d79c1a4a0887f51306e6b`  
		Last Modified: Tue, 16 Jun 2026 23:04:22 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b325315de6008bab1fe018cf4b343b3b23a249dd4634dd99e187aa5d18d887fc`  
		Last Modified: Tue, 16 Jun 2026 23:04:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f12e6baaec0472fb79f29b77d7f61a3949e9afb38fdb7760d885cc90d73068`  
		Last Modified: Tue, 16 Jun 2026 23:04:25 GMT  
		Size: 109.4 MB (109434791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10cd1562cc1e413c1a4b54800bd98bdc53f69d5c56ab338c57e1b817694652d`  
		Last Modified: Tue, 16 Jun 2026 23:04:22 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b5d62c5938a6dfbacd9c41fd5c2b544e560b8ef9a40a214f571b27a2062714`  
		Last Modified: Tue, 16 Jun 2026 23:04:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfe56a6dc1d1e97402e2e5b120248c831a366defa685cd2b5b22a26d6fcfbf5`  
		Last Modified: Tue, 16 Jun 2026 23:04:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7895926526af5a90d6a5c7aab4a0c4d74002bdc12e9ceefaadef1d958ca25764`  
		Last Modified: Tue, 16 Jun 2026 23:04:23 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d526ec18a7712ffbe9d4661a2739b3511a7334417706b3adbfb4424f995cb8`  
		Last Modified: Tue, 16 Jun 2026 23:04:24 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:ef1e841bea0eb6258b8896ef9f45726b7bd1501011d35fe3370d0b4c8f3f818a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 KB (43637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf869eaa3dad13d8c6f5d6432a89b7ab766f972a57b7f6d664f414f8aa50df5`

```dockerfile
```

-	Layers:
	-	`sha256:234c8a2bfddfe69d74860b2ad8f98f36402b026e90e3efe10c5c4cc026996cc9`  
		Last Modified: Tue, 16 Jun 2026 23:04:22 GMT  
		Size: 43.6 KB (43637 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; arm variant v7

```console
$ docker pull postgres@sha256:b47b0213de5a22cc4b358e98c4c014bb103809feb56e013c322a9106dc8a892d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107466972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52903b7f7e2ddeab9fff789161f079c112809793d175ffb3c58bd6258e448b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 23:01:10 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 23:01:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:01:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:01:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 16 Jun 2026 23:01:14 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 23:01:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 23:01:14 GMT
ENV PG_MAJOR=16
# Tue, 16 Jun 2026 23:01:14 GMT
ENV PG_VERSION=16.14
# Tue, 16 Jun 2026 23:01:14 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Tue, 16 Jun 2026 23:01:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:04:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:04:03 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:04:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:04:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:04:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:04:03 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:04:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:04:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:04:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:04:03 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:04:03 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:04:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7de71dc8b9667b504c63dedd15ee693eaa8397af84107064c2c8ca00cccbc92`  
		Last Modified: Tue, 16 Jun 2026 23:04:17 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e409d0c7a6e6c9c647dce06aa2e778b89508d4d82b8fa4de3e6a95095e7967`  
		Last Modified: Tue, 16 Jun 2026 23:04:17 GMT  
		Size: 887.1 KB (887118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bc9dee544725de8d4ba16e82b6b0f6b04934cd871a45f465b834476c69892e`  
		Last Modified: Tue, 16 Jun 2026 23:04:16 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b325315de6008bab1fe018cf4b343b3b23a249dd4634dd99e187aa5d18d887fc`  
		Last Modified: Tue, 16 Jun 2026 23:04:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d2684fb40ebe98d2aa2232b3735cdd021760273538902f0c6b9b5efae8c10e`  
		Last Modified: Tue, 16 Jun 2026 23:04:20 GMT  
		Size: 103.3 MB (103279269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ced99e6c7cca75c27e9cbb2b47ffc47ba1e92366a122cb8810145847814cd03`  
		Last Modified: Tue, 16 Jun 2026 23:04:18 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a377257778921df1298fa1ab55bb2f3313b9a5d2c72006ae405467b41902dd6f`  
		Last Modified: Tue, 16 Jun 2026 23:04:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acad5b787bbbd4e792ee725234c50160168c180a0098aaa6b2b887e607e3739f`  
		Last Modified: Tue, 16 Jun 2026 23:04:18 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8d4b7c9e52165e067c3fda95dd02a47a0ea24831b55680bdaa29cbd36ff9cc`  
		Last Modified: Tue, 16 Jun 2026 23:04:19 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8c5fbcbfd29da3eb4c8cd843f245e7079ad7a4bc8253ddf14e4cffb4f35604`  
		Last Modified: Tue, 16 Jun 2026 23:04:19 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:fc458c40485f49d819ee1f506b68f17f07308d26e1aede666442247fcf795e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.7 KB (640680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da466a9b2848c932562ff548d8a899ac7a85d71cfbaa48c41b9d88456e0eeda9`

```dockerfile
```

-	Layers:
	-	`sha256:5fcb4a5314665514da15d59cd6870e3f15b93b8c15407efb8f52e3022bd2e2ae`  
		Last Modified: Tue, 16 Jun 2026 23:04:17 GMT  
		Size: 596.8 KB (596828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5547a23c685410cafca62a7bcac2fa2ea4a1fd419de644b8cf592ebc752b4e4`  
		Last Modified: Tue, 16 Jun 2026 23:04:16 GMT  
		Size: 43.9 KB (43852 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:a52786194383471761acf32accb93bc3a870a6be3f94e553bd06df29a155850e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116165951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1809ba2d2087e42b78960132d18c236580c4d415fd92e771f9d0e64489a88b69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:58:35 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:58:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:58:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:58:38 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 16 Jun 2026 22:58:38 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:58:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:58:38 GMT
ENV PG_MAJOR=16
# Tue, 16 Jun 2026 22:58:38 GMT
ENV PG_VERSION=16.14
# Tue, 16 Jun 2026 22:58:38 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Tue, 16 Jun 2026 22:58:38 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:50 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:51 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:51 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:00:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:00:51 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:00:51 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:51 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:51 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68187b1751e44b13de8a32892f48bbf0f85f7709d27e515040489dbad3ea15cb`  
		Last Modified: Tue, 16 Jun 2026 23:01:07 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a46f73043fb8fe22a3153b0a54430f6e4a71f965677b451f5aad5da20125a4`  
		Last Modified: Tue, 16 Jun 2026 23:01:07 GMT  
		Size: 874.7 KB (874709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c70bf1a22ebd711d6d87695360ebde55c8f640957244eee74e17377e327963`  
		Last Modified: Tue, 16 Jun 2026 23:01:07 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d958084a9833e82c2171b966833ef5ad9f8cc12ccd14b63193fad1ce6b3c558b`  
		Last Modified: Tue, 16 Jun 2026 23:01:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675b42395c1b8ce8213ca3c63561a27f4cc2d44602fb24d75439bb11c98508e0`  
		Last Modified: Tue, 16 Jun 2026 23:01:11 GMT  
		Size: 111.1 MB (111073906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fd292847a7b8dbe5fe9a96ff0838ef6ac83e4ef0467e9ac9e2be0512eb5231`  
		Last Modified: Tue, 16 Jun 2026 23:01:08 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f26022f7508b5958ed6ba8e47ae52ad3f7f47bba7e6d2c88cafb7f2a6f4578`  
		Last Modified: Tue, 16 Jun 2026 23:01:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607dca6513874bcb42e98c66a3530a580d670d668eeef48d3b94c537716e32b2`  
		Last Modified: Tue, 16 Jun 2026 23:01:09 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfaf4a92aa26173230dba56f1bc1cb992fc63c77abe6b019b4dc51d6fb9c528`  
		Last Modified: Tue, 16 Jun 2026 23:01:11 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c05c3d382f46947738298288e76b73412fde74b8fd5e1c0464c6bd405f2122a`  
		Last Modified: Tue, 16 Jun 2026 23:01:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:b0bea065dc5fa4902b32a66faa137f12bd24cdbf315fb44a9cfe852fe89fe752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.7 KB (640723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ae60370b3bdc09a13bae07667d89f620ea8086137560fdc011314a7ebdae18`

```dockerfile
```

-	Layers:
	-	`sha256:2d109198134fe85978aac6c0c886980cf262fd6829e5ed8f3ef51461a9566cd5`  
		Last Modified: Tue, 16 Jun 2026 23:01:07 GMT  
		Size: 596.8 KB (596840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73b39561997489366cb31ef816718380a1b2760c4bf04cd7be3b112b9740c337`  
		Last Modified: Tue, 16 Jun 2026 23:01:06 GMT  
		Size: 43.9 KB (43883 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; 386

```console
$ docker pull postgres@sha256:720e46213ade8355623ee08bd1fc38df418b183e7c3942c892f3853d22c36feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124500965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07f1d77840eda3921317b28f7d05e7d77e9629e92bce8312d894287a8f9e27e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:58:58 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:59:00 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:59:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:59:01 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 16 Jun 2026 22:59:01 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:59:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:59:01 GMT
ENV PG_MAJOR=16
# Tue, 16 Jun 2026 22:59:01 GMT
ENV PG_VERSION=16.14
# Tue, 16 Jun 2026 22:59:01 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Tue, 16 Jun 2026 22:59:01 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:01:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:01:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:01:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:01:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:01:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:01:25 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:01:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:01:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:01:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:01:25 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:01:25 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:01:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f98aa70c035cfdbfab15d6ac3c2fb11f05043b267bc5a73b1db3a9a41a38d75`  
		Last Modified: Tue, 16 Jun 2026 23:01:41 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddc7a940641b31d082b1d1442170b8825016bbf8be3cebb30dc04539defcd69`  
		Last Modified: Tue, 16 Jun 2026 23:01:41 GMT  
		Size: 891.6 KB (891647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18197b7f58a8eee7c2a8eee9e822d8880bd63f56ea818e3a14d105a4ad001c4d`  
		Last Modified: Tue, 16 Jun 2026 23:01:41 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5a57ba19a41a2d6cc7215c141548200b658ade79552a78cf9352d1b803eea`  
		Last Modified: Tue, 16 Jun 2026 23:01:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4908c27910c52dcc2b0e74ee4512db148d05af83d3680c5b316bbca410174ff5`  
		Last Modified: Tue, 16 Jun 2026 23:01:44 GMT  
		Size: 119.9 MB (119901402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9a993431a081b1620f60bda21949211de3e6078a5a3d7d0acfce5b81ff87cc`  
		Last Modified: Tue, 16 Jun 2026 23:01:43 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06abd96da4177bdff55c5ee498ee9a11dc47473e4575fbae843be46dc15dbce6`  
		Last Modified: Tue, 16 Jun 2026 23:01:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2731de8cb2b5d87ca082393f77bc2feda19bc910ad6a686698bf9d102f5b68ec`  
		Last Modified: Tue, 16 Jun 2026 23:01:43 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a49ea2b385af61740fe39d06ed95d655708199c6ec90c86f89585d3f99d5`  
		Last Modified: Tue, 16 Jun 2026 23:01:44 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12a7c52ff96a34531f6ee6908a7d8178c4c88dce360ed66f692ce590ad74cd`  
		Last Modified: Tue, 16 Jun 2026 23:01:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:82cb5076635958c2f4123addb7e26ff6684de7218c4db418580f9de14fd547f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.1 KB (641087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89cc86ba8a23c7f064d6acddef3e06c29db52cf735ad82e6626b89eade4431cf`

```dockerfile
```

-	Layers:
	-	`sha256:ba7ab5e0966bc238f2f00463ce3b114093671c7515c229ae181cf21783160a1b`  
		Last Modified: Tue, 16 Jun 2026 23:01:41 GMT  
		Size: 597.4 KB (597443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af644c1046253af5e4687be08784525089f30b414f53e38e3ed2a9a692b21b64`  
		Last Modified: Tue, 16 Jun 2026 23:01:41 GMT  
		Size: 43.6 KB (43644 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; ppc64le

```console
$ docker pull postgres@sha256:4f3d90673298de2e6884736cafd9b732029c443a9b36471fd3332af1c67eda6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120589470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165ef728049a713ae4425e1a5103176e0c65e8354ad341605b2ec8e7f4332a22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:56:25 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:56:30 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:56:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:12:17 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 16 Jun 2026 23:12:17 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 23:12:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 23:12:17 GMT
ENV PG_MAJOR=16
# Tue, 16 Jun 2026 23:12:17 GMT
ENV PG_VERSION=16.14
# Tue, 16 Jun 2026 23:12:17 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Tue, 16 Jun 2026 23:12:17 GMT
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
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeb214de6218b60491f673adf9db82be71ea034b0f77f7368c52371e738b5b2`  
		Last Modified: Tue, 16 Jun 2026 23:01:33 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6afa0b71083646c91abee705158ea148e7247c5befb4dabd9b4d97a65cfb4b`  
		Last Modified: Tue, 16 Jun 2026 23:01:33 GMT  
		Size: 880.1 KB (880129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7dc9075476752581871bf4555e4ec79248bb50eedb71e017dc0fbcc04f10b6`  
		Last Modified: Tue, 16 Jun 2026 23:17:01 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c338e19fd96ff8a177a4f2c72eed08e5e5ccef0f44ea4d74c0557397ddf73c9e`  
		Last Modified: Tue, 16 Jun 2026 23:17:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e879f6da5daad80b9d9e7bab8e282f9194c57152ac21cd93dee51e305441d9`  
		Last Modified: Tue, 16 Jun 2026 23:17:04 GMT  
		Size: 115.9 MB (115860933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19768d950846ccf14cb6987ad3cd15003f10c82de49f4e485e3d82aa74f50484`  
		Last Modified: Tue, 16 Jun 2026 23:17:01 GMT  
		Size: 9.6 KB (9629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e5de0d4257fe63cde2ceaf4e8248b1220a46e13a622069a633cf79474efd3c`  
		Last Modified: Tue, 16 Jun 2026 23:17:03 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29011e60dd0ccbfb3b8dea4448b706eb4e8125cb45f8dc0734e34eb64ccb203`  
		Last Modified: Tue, 16 Jun 2026 23:17:03 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc91c6bb2bff0ea0a0c48dd71911f1abda5c176d38843c4546c7a5a4d397624`  
		Last Modified: Tue, 16 Jun 2026 23:17:03 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530218b1075e17fcbde5a9998899a07cabfa554421c407db4db021399397a749`  
		Last Modified: Tue, 16 Jun 2026 23:17:04 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:b06704a824afbc676ca635d01fb2bd0c95554e1526d58eaac958eb954d98a9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.9 KB (638899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a7c0b11b33786a4c74321db60a8acd20d1da124481f7d6e4056ec07e31fa48`

```dockerfile
```

-	Layers:
	-	`sha256:601749a2887ba3cf0980134c9e765f483e8ec8830d0b68eaece83cb51c72fb0e`  
		Last Modified: Tue, 16 Jun 2026 23:17:01 GMT  
		Size: 595.2 KB (595167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1939ed79d0100681e4ab62f9ac087e2b3082fa70aadc2dbb59db7bf5eaad5118`  
		Last Modified: Tue, 16 Jun 2026 23:17:01 GMT  
		Size: 43.7 KB (43732 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; riscv64

```console
$ docker pull postgres@sha256:ee4ccd4e78ff7decdefec4b05f3205392340cff13de9305c1465231abb132312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119782328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff945168a96bcf7922ff52231f578c356e2e3a3af2dc971262f4c7f7216b7e07`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 17 Jun 2026 21:19:07 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 17 Jun 2026 21:19:18 GMT
ENV GOSU_VERSION=1.19
# Wed, 17 Jun 2026 21:19:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 03:03:42 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 18 Jun 2026 03:03:42 GMT
ENV LANG=en_US.utf8
# Thu, 18 Jun 2026 03:03:42 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Jun 2026 03:03:42 GMT
ENV PG_MAJOR=16
# Thu, 18 Jun 2026 03:03:42 GMT
ENV PG_VERSION=16.14
# Thu, 18 Jun 2026 03:03:42 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Thu, 18 Jun 2026 03:03:42 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Thu, 18 Jun 2026 03:55:58 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Jun 2026 03:55:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Jun 2026 03:55:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Jun 2026 03:55:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Jun 2026 03:56:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 18 Jun 2026 03:56:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Jun 2026 03:56:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 03:56:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Jun 2026 03:56:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 03:56:00 GMT
STOPSIGNAL SIGINT
# Thu, 18 Jun 2026 03:56:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Jun 2026 03:56:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65f72f9dc4191057d4290d81d3e9b85a1e898cd4566300956d6f215da3e5d2b`  
		Last Modified: Wed, 17 Jun 2026 22:15:32 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfbfbc6e54c945a01fa3a875eb6f9cecc112c80d1bfc687accbcd8cac7b9050`  
		Last Modified: Wed, 17 Jun 2026 22:15:31 GMT  
		Size: 867.5 KB (867539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4868e08303f3ddaa412c1cd52bd5e1fd4569886a8e32528ce35b46f99b80ff45`  
		Last Modified: Thu, 18 Jun 2026 03:58:59 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3402a6f16d46d36de60b71e93cca037532b044ba901b21c2743a638ce5d658d0`  
		Last Modified: Thu, 18 Jun 2026 03:58:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f42bc6ac6927d33239417e1e5303f9743219b96e1685754416504b3a767f08`  
		Last Modified: Thu, 18 Jun 2026 03:59:16 GMT  
		Size: 115.3 MB (115309659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266e27ddebabb78a43bb6dd9e30a237d0c110c9a89fd7b6e8435b871cdb9b1c3`  
		Last Modified: Thu, 18 Jun 2026 03:58:59 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be15c1e1659eb9848c69f0a4a41b90316526a8d405ef1919227a8e9f0833956`  
		Last Modified: Thu, 18 Jun 2026 03:59:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165448e92a30c16a91ea4d73788ecde2b0208cc0f115e11cfad5f5f503f7b446`  
		Last Modified: Thu, 18 Jun 2026 03:59:00 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6e34134c34b27fa37baec3092135f154bbdc757fd0e6c11e2ac514e48c038c`  
		Last Modified: Thu, 18 Jun 2026 03:59:00 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0a524f3dfbbd73999d35cb6bb2cf89b2dd14e95e4f53867c5c9b67f85e9e83`  
		Last Modified: Thu, 18 Jun 2026 03:59:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:39c33a18c3fda1cf5ad14a568b0dad962df32055df2fd7e8cc850354669f9e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.6 KB (640557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d706ca1db970e4575a75140ec90441ab7c91661c145626e04d937a5170ce8c8`

```dockerfile
```

-	Layers:
	-	`sha256:defc228095802429997551e22139fcae774da60b4139cb60612a9fb6775a6eac`  
		Last Modified: Thu, 18 Jun 2026 03:58:59 GMT  
		Size: 596.8 KB (596825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcb67b6b961f3cdda992cd986688da770169a4ba6fc278156aa9cf46ef72edf3`  
		Last Modified: Thu, 18 Jun 2026 03:58:58 GMT  
		Size: 43.7 KB (43732 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; s390x

```console
$ docker pull postgres@sha256:8f4f2014d2a90f22c486b0f5dc090dc0f1fe45f2e515b35aae5923f7c031f345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124295042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818da603224431d99ce7a40eb9320f0e88352e5614f9d956d128d54e93867838`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
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
# Tue, 16 Jun 2026 23:06:31 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:06:31 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:06:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:06:31 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:06:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:06:31 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:06:31 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:06:31 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:06:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:06:31 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:06:31 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:06:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138f17cbec7383c2f4e65ac61d6338f7eaa0091aa05691e282fa28a8f1f0806a`  
		Last Modified: Tue, 16 Jun 2026 23:01:46 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc13189f654454854b34853fccf423aefa764a77d0f758bd423b7bc8cb09ac`  
		Last Modified: Tue, 16 Jun 2026 23:01:46 GMT  
		Size: 895.8 KB (895799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bce28ead2703fc8b8b38f2b1d7aedcd655492745241822eff7dad4df6f6c8b1`  
		Last Modified: Tue, 16 Jun 2026 23:06:57 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c5dd37845c73dafd37443171cc6c2df467255dc46daa591bd1c37afbb9b189`  
		Last Modified: Tue, 16 Jun 2026 23:06:56 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc9893d60d84c49ec3e037ceecbe0dda948a3ab05f3cb38f0613514880e3734`  
		Last Modified: Tue, 16 Jun 2026 23:07:00 GMT  
		Size: 119.7 MB (119655253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ee799658b4373bd614965671d0c3f6fc10051969baa9478a77e62d377b482f`  
		Last Modified: Tue, 16 Jun 2026 23:06:57 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306a4be26637d36f51d7896e8b82968e3aee9dc839265041bae42ff940ede007`  
		Last Modified: Tue, 16 Jun 2026 23:06:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3f7e639abde9e0ed2fa2639732acb6828d43d8ccf696d765e7769a138cf830`  
		Last Modified: Tue, 16 Jun 2026 23:06:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3ae12430ee32e2416ce7f21d40cbf845f2223a30f06ec52caac89d33be796`  
		Last Modified: Tue, 16 Jun 2026 23:06:58 GMT  
		Size: 6.1 KB (6093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275e3ee76ba7da289205b592f182bbafc6352c758e341eeeee85a5e049fb5584`  
		Last Modified: Tue, 16 Jun 2026 23:06:59 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:29642de6dc04c16f51765db2beabd922b576b7ed773b2631658a5b37a3ec5db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.5 KB (640491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5505f54c7fc901f9c564814f274fa9eeacf9a5231fbbe4498d000e31c7d1a354`

```dockerfile
```

-	Layers:
	-	`sha256:f8da4bd60bc59eb36eced205dc3205757937c5d8e9b64f3257f1da4af7111b28`  
		Last Modified: Tue, 16 Jun 2026 23:06:57 GMT  
		Size: 596.8 KB (596807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2017ea4389ab958495e9c49808a5dfb20e5773576d33ea3b81fffd05bc35a0c3`  
		Last Modified: Tue, 16 Jun 2026 23:06:57 GMT  
		Size: 43.7 KB (43684 bytes)  
		MIME: application/vnd.in-toto+json
