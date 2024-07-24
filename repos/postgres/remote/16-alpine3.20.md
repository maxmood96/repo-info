## `postgres:16-alpine3.20`

```console
$ docker pull postgres@sha256:36ed71227ae36305d26382657c0b96cbaf298427b3f1eaeb10d77a6dea3eec41
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

### `postgres:16-alpine3.20` - linux; amd64

```console
$ docker pull postgres@sha256:ac5dfd145382caa043363d9ebd5823134f0c20017c87b11a1ffcd1fa64f52500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96869381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01100f48660a46a6c3fffb71f672da75347bb12f7b264dee381cf0e985d9e63c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Jun 2024 20:57:56 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV LANG=en_US.utf8
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_MAJOR=16
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=16.3
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 03 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGINT
# Mon, 03 Jun 2024 20:57:56 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f325da6b46565519abb5d94049854dc78a4828450f58e3d15fdde754ec729c3`  
		Last Modified: Mon, 22 Jul 2024 23:10:31 GMT  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9c004462cc3c70c3949c63f609cbd3c2b9884eab94a4d2f45b7848f569a789`  
		Last Modified: Mon, 22 Jul 2024 23:10:32 GMT  
		Size: 1.1 MB (1119780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79435b3f24eb1652d4af1d23442c09e8e715ad834fc894665a271c9534e4eb8`  
		Last Modified: Mon, 22 Jul 2024 23:10:31 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826bb0ac100468a29551c8f05ac0b0fc51742843d4431db1ac9c0b245a4c66b9`  
		Last Modified: Mon, 22 Jul 2024 23:10:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877cab0f2b20b3216be0b74c2533ce470ac014006d858f363cd33e62660022a4`  
		Last Modified: Mon, 22 Jul 2024 23:10:35 GMT  
		Size: 92.1 MB (92109976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc019278051cafb6f382283d71020be0fc0a922b3c45beb0b1f9cf529643f95`  
		Last Modified: Mon, 22 Jul 2024 23:10:32 GMT  
		Size: 9.6 KB (9563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b290b70c03cd032df4485af30a408f705d3145b3a5bb413cf118eab700a815f`  
		Last Modified: Mon, 22 Jul 2024 23:10:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5349cd158aa93786351f0710807fb3ae8ad0376dbaf452330d3baaf7df4d0aab`  
		Last Modified: Mon, 22 Jul 2024 23:10:33 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45300484531de003beea89e361dde4b9960e2ec5d86f81b7d9ada916b8be002`  
		Last Modified: Mon, 22 Jul 2024 23:10:33 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40d58adb5bb3b8252ae4750499a8ec9148e8ed424ddb80c2bc161a1a62aec13`  
		Last Modified: Mon, 22 Jul 2024 23:10:33 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:438f171b8f15eff94f31dc9f2f02d4fdaabe3fd5acdf211ef2682b0f498d5b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.4 KB (637376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de40c1331d49a624476dcc17a0d57ade17af05544bf555f9de2887d60ea37113`

```dockerfile
```

-	Layers:
	-	`sha256:fcfe0967106e66dd7f2fa5b776d32fd773f586ebce6fc122c7016e2468cab27e`  
		Last Modified: Mon, 22 Jul 2024 23:10:31 GMT  
		Size: 591.3 KB (591327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5359e10dce8119d40f73d41d7148cd2f059133d845b8b9dc15254d34dc4b6c7e`  
		Last Modified: Mon, 22 Jul 2024 23:10:31 GMT  
		Size: 46.0 KB (46049 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:259720b20e1e6bcf4ec232a9c324d05f39ba0fb354628cd7e0b8d6755523a550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95573747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ced4e8df4573b4736dcd68aa945202e6c9c7849e1190346a341b14ae98ee9ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Jun 2024 20:57:56 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV LANG=en_US.utf8
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_MAJOR=16
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=16.3
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 03 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGINT
# Mon, 03 Jun 2024 20:57:56 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b773cfc448de5399b645e9021d9feb73e5260f6a55c6f74a72e816b47345f3`  
		Last Modified: Tue, 23 Jul 2024 07:29:49 GMT  
		Size: 981.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285b19070c31caa9d2c26bf36838d9bfed23a66bc19e14687cc69cefc8b9ec0e`  
		Last Modified: Tue, 23 Jul 2024 07:29:50 GMT  
		Size: 1.1 MB (1086469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb2963a2892e4a8937d2c3d799cabf53b5a4cb1c5ce1e26499c2cc226746c20`  
		Last Modified: Tue, 23 Jul 2024 07:40:10 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdeaa90218771d2c7a549b14ad1d87aae71cc65461651067ca6d60180581f944`  
		Last Modified: Tue, 23 Jul 2024 07:40:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3afde209ffd9717dce5f8213febb1e8b1244fa690d2948490e7fe29c88adecb`  
		Last Modified: Tue, 23 Jul 2024 07:40:13 GMT  
		Size: 91.1 MB (91105352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8def22b66ca27bbfbb44c48913a6828b42e7d0801db13f9c7d7356d748c58470`  
		Last Modified: Tue, 23 Jul 2024 07:40:11 GMT  
		Size: 9.6 KB (9562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b3bc042e085fe6b365ba4afef0be1c10ee4b32407679ad9648134f8633a923`  
		Last Modified: Tue, 23 Jul 2024 07:40:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b99bce4f85b8c9a3e170ff2064bd42847c86a7ba033a8e348298358359313a0`  
		Last Modified: Tue, 23 Jul 2024 07:40:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33303268a45bd69deb85768dc6eb4e0ea3119fb48fb1ceda546621086d079946`  
		Last Modified: Tue, 23 Jul 2024 07:40:12 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e95c8e2002d238e09e38cd2e93f37a50779a380efcc90a349d1324f2d8b196`  
		Last Modified: Tue, 23 Jul 2024 07:40:12 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:18c4e4bb2c9c4007982c912cddada4599a7802a70e580d2373dc1176188ba447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 KB (46020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364c64305b35b3aca605514edb8980bb4a80a592d2c965c9139128af92d26577`

```dockerfile
```

-	Layers:
	-	`sha256:4dca1898bab4c1231780e25b0fa4f29d2776a59f1af8b0129f52137a64802b5e`  
		Last Modified: Tue, 23 Jul 2024 07:40:10 GMT  
		Size: 46.0 KB (46020 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:7a14646d115c53d1739f5e817b7708991c4ae7d16786d11e2131e8ae1fb0ec77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89979389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d812e953c69a70a9ab98fa3ee30a3f968af96c38b2346674a9be8d41569c236b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Jun 2024 20:57:56 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV LANG=en_US.utf8
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_MAJOR=16
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=16.3
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 03 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGINT
# Mon, 03 Jun 2024 20:57:56 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2490af644d68c34906e0c9e80c2e13f2de007edb89b5cb5a48d745b862813731`  
		Last Modified: Wed, 24 Jul 2024 03:43:18 GMT  
		Size: 981.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e95c854f037189d46203de85a8267a4b5195f503635dd6f6bb17821f554e94b`  
		Last Modified: Wed, 24 Jul 2024 03:43:19 GMT  
		Size: 1.1 MB (1086472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cc9497a5a3a57e7e22e03d57e578257b2154fcef7e619e8fc4f53dd99c4091`  
		Last Modified: Wed, 24 Jul 2024 04:20:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f74dbf7a2139887bc137c0aa3958db7419a82683fa84c0c3b96c34b167dead6`  
		Last Modified: Wed, 24 Jul 2024 04:20:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77de4573f278a93b0becdfc5855850bea14940d1021d21e305c777f35f19f3f2`  
		Last Modified: Wed, 24 Jul 2024 04:20:40 GMT  
		Size: 85.8 MB (85781229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b194ecff09464bb8ffc1af7cd100cf0297ce8370092a445ee7c5f7820c02ae68`  
		Last Modified: Wed, 24 Jul 2024 04:20:38 GMT  
		Size: 9.6 KB (9559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be02c9b3bbc87ba7eedfcb1a1a2b6c7e415732d5414e26b2f7767ec5dfa2f434`  
		Last Modified: Wed, 24 Jul 2024 04:20:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee78a58b6e9e5e0682b4d461e18932db1e0e0110cc3fa45edd8e257b25aaaaa`  
		Last Modified: Wed, 24 Jul 2024 04:20:39 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e24b9777514e0320d0e22327d89b0342bee6944a3ab261b14a0da38187a2c1`  
		Last Modified: Wed, 24 Jul 2024 04:20:39 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015a7e55488e772e70299f351d660ff0e65ce2eff07ac5764eb48ac0d9cb9f10`  
		Last Modified: Wed, 24 Jul 2024 04:20:40 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:5e06c41311f140d07970f262f6cc8b12dec233cef215b9776f4490a27f73f904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.6 KB (637618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555c525475b6ea0880d0522a83e0772f1acc5bd01d9393974db3f9dfa0db8270`

```dockerfile
```

-	Layers:
	-	`sha256:baffd2744483bb2afa916a49e5b6bf49ada9f4cf6abab8619969da0e9e0a33b0`  
		Last Modified: Wed, 24 Jul 2024 04:20:38 GMT  
		Size: 591.4 KB (591379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19f1ca39b2e07494c770673d4079801f86c568a17c6dc8387ccb753b34dbbaf3`  
		Last Modified: Wed, 24 Jul 2024 04:20:38 GMT  
		Size: 46.2 KB (46239 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:f6a26cc31186c48ade9b37ecef50e8fe0bb86d381440cc19155831615697540d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96091711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d3b957702a1b159492df69e328c7ef2d0d2003c03bb4e7c9ee53bf8881c3aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Jun 2024 20:57:56 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV LANG=en_US.utf8
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_MAJOR=16
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=16.3
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 03 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGINT
# Mon, 03 Jun 2024 20:57:56 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27fb9865e4405c08712daac8b15112b58371c98aca70a1d04c881d9f6e87c23`  
		Last Modified: Wed, 24 Jul 2024 01:21:01 GMT  
		Size: 981.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c039ed13e5edff36f72afe54a34f3989ac3fc60459e2652266165351ec1637`  
		Last Modified: Wed, 24 Jul 2024 01:21:05 GMT  
		Size: 1.0 MB (1047251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cffd2df61482f46795d2e01617b50eca723eeef6292f9b065d4e9d35e8d14f7`  
		Last Modified: Wed, 24 Jul 2024 01:29:42 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80738f4d19d54af2826e200709a79b256920178a94e80bd70af2e516ed691ee`  
		Last Modified: Wed, 24 Jul 2024 01:29:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e750b6363364b0ea767224b594deaa7dc6fd6e9c142619e523b557f86068f95`  
		Last Modified: Wed, 24 Jul 2024 01:29:45 GMT  
		Size: 90.9 MB (90940792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538d306a146472e71a6fc739add07e343f4419ea4b7a44a6e7f1969ff0e42025`  
		Last Modified: Wed, 24 Jul 2024 01:29:43 GMT  
		Size: 9.6 KB (9562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1beddae2772cd431193dc4e7bfe2bc1a93fca7399171deea6df95cae18fa4c6`  
		Last Modified: Wed, 24 Jul 2024 01:29:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a579755e21ba461d25576b672f2d8d19403dedb55d56a02827029c105b89aaed`  
		Last Modified: Wed, 24 Jul 2024 01:29:44 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec2ac09a5ade2bb28a061083b260e4a199b79eeb8a1e7a053504a5bac44ec57`  
		Last Modified: Wed, 24 Jul 2024 01:29:44 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d54fb5d4611bb56429a4b54e718f59a240171aaf8ca0989af8e975a11f81c0`  
		Last Modified: Wed, 24 Jul 2024 01:29:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:d69046cea6fbdb08359cf4cafd869860fe9ccc6c284cd1de2b18886028d723f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.8 KB (637780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9aae9da273e698814f762e09701df8100027147ef25733dae199f2636252f2`

```dockerfile
```

-	Layers:
	-	`sha256:1c419a290fab6d18765321d615a40435cae9c7bd5dc9d98adf01a65b2ffd5258`  
		Last Modified: Wed, 24 Jul 2024 01:29:42 GMT  
		Size: 591.4 KB (591407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82b18cb6a4e7159267ad355b8346e30e3e7f4497cd1cf499c72d55ffc8b26777`  
		Last Modified: Wed, 24 Jul 2024 01:29:42 GMT  
		Size: 46.4 KB (46373 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:a5b68757566ec99e042155e51dccd2db1293ddcccb4665a738617c09b1ed19eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102172483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e295208769782f27f85b1e9f97da127813f6a70fc4aaf584e6ebe4afcde1f11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Jun 2024 20:57:56 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV LANG=en_US.utf8
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_MAJOR=16
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=16.3
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 03 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGINT
# Mon, 03 Jun 2024 20:57:56 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54506773fbfbf5f51fd024075ec96b7c34c65afee8208af92564c49b3ca745e1`  
		Last Modified: Mon, 22 Jul 2024 22:15:00 GMT  
		Size: 981.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7152ccde47bdd2a8319723d8f3623a02bdba59cd3916b303865ed47d9fb0490`  
		Last Modified: Mon, 22 Jul 2024 22:15:00 GMT  
		Size: 1.1 MB (1094853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e382e52c03115b0454e4e0f3bb5dc1133d93abb72c01265e843ba189c098df0`  
		Last Modified: Mon, 22 Jul 2024 22:15:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7988cf249b0e1dfcb76a147c9554d9318a60dcc5d3ab9bc6187fb232c09ce9dd`  
		Last Modified: Mon, 22 Jul 2024 22:15:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96773b172a0bd7e1971c0568944d1db32e9880582b9c89299844afed929c3d4f`  
		Last Modified: Mon, 22 Jul 2024 22:15:04 GMT  
		Size: 97.6 MB (97592836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901599347d869e173732bc739af6aa0a322674899846a8b09643305875048ff0`  
		Last Modified: Mon, 22 Jul 2024 22:15:01 GMT  
		Size: 9.6 KB (9558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614042e6755917c1ef0ed6f4160189d437ea31f47b336227cf12bee5dd2dde8c`  
		Last Modified: Mon, 22 Jul 2024 22:15:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48ed2d40e631e929329b1ddb6d65a8fa1eb2ea04ae1e9d8f81926297ee80183`  
		Last Modified: Mon, 22 Jul 2024 22:15:01 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad87e97964650541249bda92083b446e08ea069dc37cc7e8b19b4566a11ff191`  
		Last Modified: Mon, 22 Jul 2024 22:15:02 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9777d18ddc75a4dd13b8baae678c81c57ae351ad6bcff871916da445de65b`  
		Last Modified: Mon, 22 Jul 2024 22:15:02 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:f0c15109907b2d7244e78f4a101bf19f71d0c5966ed06782de5f29e2ac37cd88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.3 KB (637286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e9cba2237264baad182e490fa3b25c7b79c3228198be3dcf8f3ca333c0642b`

```dockerfile
```

-	Layers:
	-	`sha256:5d083ec8cb59b28ee1b7d3a032166a0a258cb6e8b8234450a1a1b26aeddb357c`  
		Last Modified: Mon, 22 Jul 2024 22:15:00 GMT  
		Size: 591.3 KB (591292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f7e7b7125ef96ff9fc9211ed977cb5e7161d3120f2915859821f34b5610d3e5`  
		Last Modified: Mon, 22 Jul 2024 22:15:00 GMT  
		Size: 46.0 KB (45994 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; ppc64le

```console
$ docker pull postgres@sha256:fb24f4cca56d687cfbc023ccb5854e970c0db2749f30aedc963fd742652f2ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101452820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798da4973043182bb7d0c208587c339bcdea45d672903ef1a35b828c0801d939`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Jun 2024 20:57:56 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV LANG=en_US.utf8
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_MAJOR=16
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=16.3
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 03 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGINT
# Mon, 03 Jun 2024 20:57:56 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a1d1dfa6c48946d1f9317d8f93d0b7895f5351dc2a6503d7cc52630a782071`  
		Last Modified: Tue, 23 Jul 2024 23:20:06 GMT  
		Size: 981.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6514b5dc047cae315f0f38652a7ac042c49b38dc103a5e1c2370e8652127623`  
		Last Modified: Tue, 23 Jul 2024 23:20:06 GMT  
		Size: 1.0 MB (1037914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e46b0e542a81e9887e376b49bb1022646a57cde9d939e5a381e7534b3091f25`  
		Last Modified: Tue, 23 Jul 2024 23:30:04 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e82942e21eea2504b4605ad7e8b1ddb3197434addddc2a7d27be3293c7159d`  
		Last Modified: Tue, 23 Jul 2024 23:30:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4605e755d6599834651c5a2d719fe60e0d30c3a24d7eada532998e5a5455f2b4`  
		Last Modified: Tue, 23 Jul 2024 23:30:08 GMT  
		Size: 96.8 MB (96826610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39726fb17ce2b539cea46f1dc36c04da45ec6ec091a05960b8bf1cb5c42ffdc`  
		Last Modified: Tue, 23 Jul 2024 23:30:05 GMT  
		Size: 9.6 KB (9564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39b34ff6b203613f7d6356ab571053c1d51696782c08afa9898b552bca2a7eb`  
		Last Modified: Tue, 23 Jul 2024 23:30:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcba08471ac4b7777b053ed39e8fcdcb938ee9fbaa4aba6099e63b921cae3967`  
		Last Modified: Tue, 23 Jul 2024 23:30:06 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6879e492ea917b20897e39e9cd7d7578ee190e795c1728dc0fa7537ed0dfdf65`  
		Last Modified: Tue, 23 Jul 2024 23:30:06 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3aab2b062f21a1f3320fe6fb3529b070416af3f7d8da1ff7c683066af85aaf`  
		Last Modified: Tue, 23 Jul 2024 23:30:07 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:d59ab38397e923b1e3eeac67e5be4ffccfb8550c06cff10377136b36e3e3c870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.9 KB (633870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53ef69dae6f59ac03d7673a019d15fbff497e7b510c8cd952b7838244611076`

```dockerfile
```

-	Layers:
	-	`sha256:49f292dc96d92e67c87331103a30a6376b1f533d4e220094121f62595dbfcb0d`  
		Last Modified: Tue, 23 Jul 2024 23:30:05 GMT  
		Size: 587.8 KB (587755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:798cd1523d1eee05e16daad9be56f50d5261ef48ace15bf7357609e8f104ae94`  
		Last Modified: Tue, 23 Jul 2024 23:30:04 GMT  
		Size: 46.1 KB (46115 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; riscv64

```console
$ docker pull postgres@sha256:2e4046d2e414ec4183126f73cdfb7e33a0171b9fa58fe3a770c5debee7cca0a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96975481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7b6a1fddc9e9cf5fe52af2ddb311c3a256a8549899f461dd8c55f68dd29d4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Jun 2024 20:57:56 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV LANG=en_US.utf8
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_MAJOR=16
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=16.3
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 03 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGINT
# Mon, 03 Jun 2024 20:57:56 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f9c8f85171d26aeda06c9d355f11f8beef2f03f9009a826bad2acadf10ca95`  
		Last Modified: Tue, 23 Jul 2024 21:21:02 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef062b8f1847584965c8e6bde2c4c8e1418d7863f2cea583462d86268ad7913`  
		Last Modified: Tue, 23 Jul 2024 21:21:03 GMT  
		Size: 1.1 MB (1087949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec68fe972566af5bb9d30a0b852757b04bbf4b9d1ad0feb39f5edfec263570a3`  
		Last Modified: Tue, 23 Jul 2024 22:10:53 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afd77d6111a7fb2655a327259ac6078cf839f5d45e17b37cab1b2314ecc37c5`  
		Last Modified: Tue, 23 Jul 2024 22:10:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1353d990f25a02d158ba762f5242148c4e6053eb6590f502a717358dfe88531`  
		Last Modified: Tue, 23 Jul 2024 22:11:06 GMT  
		Size: 92.5 MB (92500112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fa77a58d319527d62c666230abed01ad9263ce748b15d68443d4692822167d`  
		Last Modified: Tue, 23 Jul 2024 22:10:53 GMT  
		Size: 9.6 KB (9569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3851d2a1945ef562867ba0825a1239d95585ef85336ffbedfa39ac565e29edb6`  
		Last Modified: Tue, 23 Jul 2024 22:10:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9567e261d9377cba51cb777c586ab2a24edf684ad534d9f5e0f8ca868f336403`  
		Last Modified: Tue, 23 Jul 2024 22:10:54 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d8a663f4f4c1bc862d2895e69fe039df647b585045031d4d1fc6936b0b8781`  
		Last Modified: Tue, 23 Jul 2024 22:10:55 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e76e9c6358de79fb2523f01a8f63309a7f670d9936c76c01b840ba92aea6bc`  
		Last Modified: Tue, 23 Jul 2024 22:10:55 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:d1c0206183eeb8ca092fb9d55ec838efca782b65a7bd22d0dfafadaa7a153e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.5 KB (635530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca70ff3d925f91e9c023fe02be708e58a78a2c5f86b7ad1d88176a1a455a7768`

```dockerfile
```

-	Layers:
	-	`sha256:87a3365baa46a661cecec476ac1017bb4c25790d440c4cb1e94d2f0f8463a8a6`  
		Last Modified: Tue, 23 Jul 2024 22:10:53 GMT  
		Size: 589.4 KB (589415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d24d937311ba3312ea9f8c0cb1007f58d17fd5da509ae2fff7dc6dfde81c18f`  
		Last Modified: Tue, 23 Jul 2024 22:10:53 GMT  
		Size: 46.1 KB (46115 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.20` - linux; s390x

```console
$ docker pull postgres@sha256:21b359bb1a5a113b689b8fcbcd101650c221e785a30bc99703abe7e33ffa856a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105771342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd0ffc22ccb229c6b861f1a924ac81aac1e2e0094e0aafa0c9ff00f0b9e6a01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Jun 2024 20:57:56 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV LANG=en_US.utf8
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_MAJOR=16
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=16.3
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 03 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGINT
# Mon, 03 Jun 2024 20:57:56 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4eeadcd529d3c2a66e80871a9e5de83052ae345a6019e2b8fd981daca9c5e7a`  
		Last Modified: Wed, 24 Jul 2024 02:25:23 GMT  
		Size: 981.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44083bfdacae2a86795f5b24627c357ad49ca12ccc52a334e42eeb5f1ef2a0f5`  
		Last Modified: Wed, 24 Jul 2024 02:25:23 GMT  
		Size: 1.1 MB (1083302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03cf4b3d496cb1b837b4ae7b142ceb6d6facbc3952537cdf7b801f78cc45736`  
		Last Modified: Wed, 24 Jul 2024 02:37:33 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8789d7dc34fe1be7a22b1715abc1e7103ae641ceceac532f18687fab50d23c`  
		Last Modified: Wed, 24 Jul 2024 02:37:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d8a1592f5375480c0b740fed5f1963af8376ed8fc8cef7baa260534ab0d430`  
		Last Modified: Wed, 24 Jul 2024 02:37:35 GMT  
		Size: 101.2 MB (101210233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e49475869e1e551c5c771ab5dffee07d567d81384273ef64e91df239f7b46c8`  
		Last Modified: Wed, 24 Jul 2024 02:37:33 GMT  
		Size: 9.6 KB (9564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97bf4dce0b8d7450e3cb1ae090ca6c33dee9f629e0d3767f32086c174d182c5f`  
		Last Modified: Wed, 24 Jul 2024 02:37:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67feb5303dce73fd099c435db7651452f1bdb45e1e340458a4618998bd4a5691`  
		Last Modified: Wed, 24 Jul 2024 02:37:34 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4786e0a42c33d2262665e174714fb71dc7213be57f30a33d67de49c31cc410c`  
		Last Modified: Wed, 24 Jul 2024 02:37:34 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4ea5638924dddb39a9bf376b5299d70bed351eee30d877e51b036018630a87`  
		Last Modified: Wed, 24 Jul 2024 02:37:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:28de0581161c2409a4d5c905b94d95ea0ab6b079233a69b725e2630233f7344a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.4 KB (635427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a720ad3a64e6336e1165968d76001f860117787fc70d512030a211abdcde1a0`

```dockerfile
```

-	Layers:
	-	`sha256:809ba11f484037530447056af269fc4b27ae35e54dd8ab626503873b906e7778`  
		Last Modified: Wed, 24 Jul 2024 02:37:33 GMT  
		Size: 589.4 KB (589373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba67dd3a6afa82dcdb2c0296536aaf8c8e74ff973837079e21a3d183681b99ca`  
		Last Modified: Wed, 24 Jul 2024 02:37:33 GMT  
		Size: 46.1 KB (46054 bytes)  
		MIME: application/vnd.in-toto+json
