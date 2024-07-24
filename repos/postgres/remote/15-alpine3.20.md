## `postgres:15-alpine3.20`

```console
$ docker pull postgres@sha256:468d34fefd6338031787c7b8e94078975b3aaf4d66c7ead25c39cd3ba46a15c6
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

### `postgres:15-alpine3.20` - linux; amd64

```console
$ docker pull postgres@sha256:cd323413f3ec037de622fdc2724215170f32045f6ac5a940d80e988862df45ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95999348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f506c9c47418b6aea3cba83f1d922dac7cc5421646a8107f9535a9c4b6b18f22`
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
ENV PG_MAJOR=15
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=15.7
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:8d8b5eb5a9b12621b4ad279a08a45f957ab15c11b5bec65d10145b33cc01f3fc`  
		Last Modified: Mon, 22 Jul 2024 23:10:04 GMT  
		Size: 981.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6debb209f6cb5a17d56bda0aa1ef1b693d4e1db920a4f41997e6c4dfa6b247`  
		Last Modified: Mon, 22 Jul 2024 23:10:04 GMT  
		Size: 1.1 MB (1119777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c952e2e6debde4f87e0b9a86155dc851882fdda2d203a424866deb4678896a`  
		Last Modified: Mon, 22 Jul 2024 23:10:04 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db166f8056c8cd7af3866f193c01bc8f9f0721a6811766f5def05268e3b136d`  
		Last Modified: Mon, 22 Jul 2024 23:10:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0735445f078105c75e8c925776c3db6849c5dd0d97dce729b7dd192808ee1a`  
		Last Modified: Mon, 22 Jul 2024 23:10:06 GMT  
		Size: 91.2 MB (91240065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a0304d892ab4cb5a0963e5134ed99353ab279edd7d6ec4bbd2b79d1c449c3b`  
		Last Modified: Mon, 22 Jul 2024 23:10:05 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2646488f1427e51c0a9f9b459030d6c15825f7b21560a66a6737c99b1d4e8e5`  
		Last Modified: Mon, 22 Jul 2024 23:10:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8114b967721f3303e349b14ffed8f215013af143b30faaae33af171b1f9a297c`  
		Last Modified: Mon, 22 Jul 2024 23:10:05 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a098ea734958d6a38cd5e91962d80fd169c15d9c6634c1441008699081f372`  
		Last Modified: Mon, 22 Jul 2024 23:10:06 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6083ec5d0bbcabd90d8bc8d4a9114ae10ccfe22547ac1cdeba885952e1c113b5`  
		Last Modified: Mon, 22 Jul 2024 23:10:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:42b14b561659a1ba6157f901b060c840d049bbf0d34859a9105c908c0e81d6f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.2 KB (636236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3964657387cc3fc7aa5d069db612b2162471334bd14e395472341ca29ad456`

```dockerfile
```

-	Layers:
	-	`sha256:fb3c6675663e6b7c814501b0024e20536d70ae31e21b77921d2403890248c519`  
		Last Modified: Mon, 22 Jul 2024 23:10:04 GMT  
		Size: 590.7 KB (590715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fa5290de391fd31d1f6d830e8c7e024c4cb6427d43bdb8d7072375a0070f216`  
		Last Modified: Mon, 22 Jul 2024 23:10:04 GMT  
		Size: 45.5 KB (45521 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:0ffb5cf3ea73357807973f45e198025aad79cab9434c28e7de05114a356a86e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94760726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87c4235b9d93358893f1cffb40f12aae7aba49f6fdea69709900f66346b2aa6`
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
ENV PG_MAJOR=15
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=15.7
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:47c0751b72404bb94a1deedebc94d57fe5eb00023e4a100141a1cd48f3651cd0`  
		Last Modified: Tue, 23 Jul 2024 07:48:48 GMT  
		Size: 90.3 MB (90292446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12b20f0c6110fcaacffb8a58b32a95bd832b543514c4b9a1f77ab80fb42d155`  
		Last Modified: Tue, 23 Jul 2024 07:48:45 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f31fd0deacd05f42624f0c232027a6e66b11a9f5afe5ebb0996d4a39fab036`  
		Last Modified: Tue, 23 Jul 2024 07:48:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6472817d49952dffec07ac40da3c039e2cb85e444a9c39ca7b92d667e5601a47`  
		Last Modified: Tue, 23 Jul 2024 07:48:45 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d6f93c7e0e1a6dcf45854f8681d19eca525090c3983d67f665251bbaf17fa1`  
		Last Modified: Tue, 23 Jul 2024 07:48:46 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e659ed6f4c3508e087d32838603c24e12472619b2db0345e807801d336d2b6ad`  
		Last Modified: Tue, 23 Jul 2024 07:48:46 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:c11a70ba9dc0b58250e88dc504a9144650d8c3bd035b0236dc35202fa4cee993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 KB (45476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62940016d9f3712fedbdbcfe46f90bf81b02c399b04dbaba26ca41300d11748c`

```dockerfile
```

-	Layers:
	-	`sha256:d657a067a04a7fb35a6a7560496be8e1c63c227c85f1beb97953d0c4d617dd3b`  
		Last Modified: Tue, 23 Jul 2024 07:48:45 GMT  
		Size: 45.5 KB (45476 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:2e22b96d2767845128ade5735c2cacbcf7db61ab05c0bd144cac5a3ef14b04f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89185351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25173fe34cce47e10824549b6a0f670ece06af1c87045b9b6f02d8891a52c852`
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
ENV PG_MAJOR=15
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=15.7
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:18a4b3e3abf735a010d5aaf78e32548efa5aea27b3267f58804dd4814db7332b`  
		Last Modified: Wed, 24 Jul 2024 04:56:21 GMT  
		Size: 85.0 MB (84987300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667968682ca210dde1346a1a903a8567a176e95a03717243a1ba9e33666c5d28`  
		Last Modified: Wed, 24 Jul 2024 04:56:18 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ab5df9ced5f0fc9e82a47bb0b30259873b8dbb70b689901df932d7c69b1e1e`  
		Last Modified: Wed, 24 Jul 2024 04:56:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5011f9c5f2fa12feee4fb0d2d1fd329fd6394b3e288a3807a79ebf14f6d7ad`  
		Last Modified: Wed, 24 Jul 2024 04:56:18 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddccc6e3cdaa60857b0c86e97df936a252c1e0fc2a76850a5c59936b56b16020`  
		Last Modified: Wed, 24 Jul 2024 04:56:19 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5362a9c8e7fabd77b0a8b8caadff3f2cc14abd259a7b6b7b4c6e14bfa973ebde`  
		Last Modified: Wed, 24 Jul 2024 04:56:19 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:3773112fe1330f81b16f1fe65f9959e758194771a18c129faf08b808774e0be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.4 KB (636446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06246f5b075ccc5292be4e98d83ff07e9ba08d03e05d88c71573ae28d39cd42b`

```dockerfile
```

-	Layers:
	-	`sha256:3dbd0943d697bb0066733a6b8adbda392382307240f8509454c2c9c7cc9a247e`  
		Last Modified: Wed, 24 Jul 2024 04:56:18 GMT  
		Size: 590.8 KB (590751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ae7de8f92176cc700645d41cbaa90ee98f9d3ea621f3a56dd19e2dbb88d10d2`  
		Last Modified: Wed, 24 Jul 2024 04:56:18 GMT  
		Size: 45.7 KB (45695 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:a9870e090dbbc3cd28fd87d48fc9a6a5738ae9a6d438aff4f8c24a69661d0ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95221293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455832411d236a3bc44d4f39e789cfd3d7b321838662351a46bead0ef1dafd15`
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
ENV PG_MAJOR=15
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=15.7
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:61c6b0e59f38a381f904fa3ba3e9ec7dd047f92fe8d644e3e99ca65101510095`  
		Last Modified: Wed, 24 Jul 2024 01:37:25 GMT  
		Size: 90.1 MB (90070488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c647d13a3d0639835ab057df189acd3f75f072f180a23aa3765f75c2a1255494`  
		Last Modified: Wed, 24 Jul 2024 01:37:22 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab2c1a64e358f9fce7a8b487deedc7e7848131192e067d4905998f2c12606f0`  
		Last Modified: Wed, 24 Jul 2024 01:37:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f318e1d4f122b3273436c77e84084d1b4d25df947bf7267b2e61ef4fbdb9da`  
		Last Modified: Wed, 24 Jul 2024 01:37:22 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab62c681a1814cb463545f5af32f51749d87a026d68c10969cc0868dbe29695d`  
		Last Modified: Wed, 24 Jul 2024 01:37:23 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fbcf217dfd6b4e70347c4ff25ff96665823527e961f9552407c8092a3c51b45`  
		Last Modified: Wed, 24 Jul 2024 01:37:24 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:34d957aae9b5bd7cdfe656ef45bb386a51f1fd06aee1555a1297617cd97c36db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.6 KB (636592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e503b0f03ecfe4b101c426b29ca8b250d7606a2d24a3012be4a121d46e821ff`

```dockerfile
```

-	Layers:
	-	`sha256:c2f2829ae425142eced09243ff8d058814ebedd19dcf91bfd74859a00b892362`  
		Last Modified: Wed, 24 Jul 2024 01:37:22 GMT  
		Size: 590.8 KB (590771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a79f5e57139cafb18a8cf289715fdbe34b8431ba63be90e3b3e5c7b72e2d30a7`  
		Last Modified: Wed, 24 Jul 2024 01:37:22 GMT  
		Size: 45.8 KB (45821 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:0291e730a1220c8843d854d3b31ccc74dc507474bb24190fb1d1f2234bd87706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101338153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db8e551e37cdc9e22f194e244ad51c486857c4c642a223aee88e2632f42212a`
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
ENV PG_MAJOR=15
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=15.7
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:43e8bbf58af7865d9b4ad7ed74f660063dc4314cfb44ad066ab896e0f1aacf08`  
		Last Modified: Mon, 22 Jul 2024 22:15:16 GMT  
		Size: 978.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a10e6628253649d72572b9bdeac49622f97c411ebd1758bf3ae981c8ee17e5`  
		Last Modified: Mon, 22 Jul 2024 22:15:16 GMT  
		Size: 1.1 MB (1094855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21500040455b5d4bc7a2b0de5de34a90eafe9f3942de16a621827a67f2d2ca3b`  
		Last Modified: Mon, 22 Jul 2024 22:15:15 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd37197d08ee12ba1bd16b281ddca2753fc3f1368cd46ebad02ef0529f90440`  
		Last Modified: Mon, 22 Jul 2024 22:15:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff342a5160018d02a1d4ceea3b86372cefdd07e6fb314a215ca3ec8389d4597c`  
		Last Modified: Mon, 22 Jul 2024 22:15:19 GMT  
		Size: 96.8 MB (96758613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a5156bc6309080446013f89c6a09394a8dc428cbc4e1030e27b3a1088a8304`  
		Last Modified: Mon, 22 Jul 2024 22:15:16 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940b904532593ede697b893cd7a05778dd2c8a252361afa1f800417e50fc2e59`  
		Last Modified: Mon, 22 Jul 2024 22:15:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0502d186c220a300128a438f608b5181b9e2464a318595c04eb2f60a4e5f0d`  
		Last Modified: Mon, 22 Jul 2024 22:15:16 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a38e0314973987611d9897c2d3096b581d1be160b34d996f1c310bb595aebc7`  
		Last Modified: Mon, 22 Jul 2024 22:15:17 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14944e76dc061ac0d0e30318e1532a66b99cce0528d4232b9fb2406c5beebfd9`  
		Last Modified: Mon, 22 Jul 2024 22:15:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:6ce9bde466f76388c93c95b8fb2137ebe87c0bca089a761d6bafae08c6918f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.2 KB (636166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5ff9d800443105dc1ee1cf0f2bb968bfc41875658d1c8cf971e3e90223270b`

```dockerfile
```

-	Layers:
	-	`sha256:4a96fcb8bcf8545c8c3a25c1454bf14cee73da50049990a7d56f453e201f3ecf`  
		Last Modified: Mon, 22 Jul 2024 22:15:16 GMT  
		Size: 590.7 KB (590690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b5df638f49bcd0097d18f9e518f638f14d9252e2196b356a5d5e2ff018e89b3`  
		Last Modified: Mon, 22 Jul 2024 22:15:15 GMT  
		Size: 45.5 KB (45476 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; ppc64le

```console
$ docker pull postgres@sha256:88f38ecbc748516f34d78f216f139ca553e169d94209a0a62d13fcc97bbc999e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100558464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90e869628c7ce9b536734cf7efa7ab2149198e460f5cadbab7ad5ad5937802e`
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
ENV PG_MAJOR=15
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=15.7
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:cde9658a62ba6da5f5b35b5019a43b44e2a9dad29b0767c133603d0a0af1e5f3`  
		Last Modified: Tue, 23 Jul 2024 23:39:28 GMT  
		Size: 95.9 MB (95932366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086f846d6f8dfdf894f20ab73be8e4a2749c19ab238614561c62ae9db04b3b62`  
		Last Modified: Tue, 23 Jul 2024 23:39:25 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98244e63a391022721553247f7683d2fd9943968c026253fd47e4b584e6b5d39`  
		Last Modified: Tue, 23 Jul 2024 23:39:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0159c5306bbe4dacb25c5b84b7761d9f756410f7eacc899b7b034cf878caba`  
		Last Modified: Tue, 23 Jul 2024 23:39:25 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f6104d31e503866ccdd5da4d661b3c049d5207bae036ccc8a449a0d73e4e61`  
		Last Modified: Tue, 23 Jul 2024 23:39:26 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d482742410353110ae27dfb340e95aefb3eb95000fc34f8a2160a8bd7768988`  
		Last Modified: Tue, 23 Jul 2024 23:39:26 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:912cea9e503c7534dd236a346142c63e2d6870afa66417dd9a2016482b28ea67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.7 KB (632706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ba6f3919057e83a1ff36a99c042ef979fb787aad9c5e4f58edf4a45930e055`

```dockerfile
```

-	Layers:
	-	`sha256:95224e3eceb4116232b669782c82acfc7c636e01f09b58868bee82ea0652263c`  
		Last Modified: Tue, 23 Jul 2024 23:39:25 GMT  
		Size: 587.1 KB (587131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03a3b0851fb05d66b84b0eae9d78db2854c373aad6833a04a9869b2f94439e6c`  
		Last Modified: Tue, 23 Jul 2024 23:39:25 GMT  
		Size: 45.6 KB (45575 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; riscv64

```console
$ docker pull postgres@sha256:ce997e79aac230880547fe4672f27007d80434c2a0bac616d504507259de87bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96112514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b22c1752cc892722cbc13a76a3a9182b7b3cd9d92e9480cd2fd3b7e5159793`
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
ENV PG_MAJOR=15
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=15.7
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:941e9227d52cc0ffa91c4d0790f692092e59da3c3a22977dd4458174acdf1a9e`  
		Last Modified: Tue, 23 Jul 2024 23:00:00 GMT  
		Size: 91.6 MB (91637271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdd3b91597231ebfb034e57fdc33afb7e60a6dfef1a46f3a8d3748216cdd9cf`  
		Last Modified: Tue, 23 Jul 2024 22:59:48 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c521540836b5012e5989195f18b863c917dda0be596b4c76b60117c7895568`  
		Last Modified: Tue, 23 Jul 2024 22:59:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c43056f4a8ec39943fd9a92a7eaa949281cb4c5c61e57929adc14ef1207c34`  
		Last Modified: Tue, 23 Jul 2024 22:59:48 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e112c34b421feb6054758fd8ff5d111293f9123c8cab6b1e62e88ce80588e5`  
		Last Modified: Tue, 23 Jul 2024 22:59:48 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e96026e8ff184ce2632d5fbe363b361f938e646ac4ac933989f76d6feb31c`  
		Last Modified: Tue, 23 Jul 2024 22:59:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:ac7c2574e8748c15575ee5012c849270fcf3e4f157ed8f5036868b872a7d0d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.4 KB (634366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c80b4a225c51fb99aa04c54172ae52e8a9b3baf591664a980eade8f094aab2f`

```dockerfile
```

-	Layers:
	-	`sha256:3584e11be445195167385781b4915b6ece1409c621632e98af2df715e17bd01d`  
		Last Modified: Tue, 23 Jul 2024 22:59:47 GMT  
		Size: 588.8 KB (588791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7290fbf94c00896e8962ef56f043e4f3667dc8fd3cab64a746eb5bc3b85faac2`  
		Last Modified: Tue, 23 Jul 2024 22:59:47 GMT  
		Size: 45.6 KB (45575 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; s390x

```console
$ docker pull postgres@sha256:09600fc345970a5728c5549785ad7c41bdcdcffee89d7aa62fc3583c43aa898b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104901589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f4ddb30060ec06f9761436ccbbcd7f0d463f56b7cccc9d5f6663c4890d171b`
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
ENV PG_MAJOR=15
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=15.7
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:0db1fedbc0faf26b1794c15bb7ed2629922a04f7218d7b3eedd8230e2e7e36bf`  
		Last Modified: Wed, 24 Jul 2024 02:47:38 GMT  
		Size: 100.3 MB (100340594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61510c3954de01fbba2e0733dad0f143c706e396fdf2c5147c5706bf7fb20577`  
		Last Modified: Wed, 24 Jul 2024 02:47:37 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59771d3f1cb52b30467831f56e5d6689d50daeb7cd366f9d06e0872d6dc120a`  
		Last Modified: Wed, 24 Jul 2024 02:47:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a4dda8e7984ab0283a5bf4ec2bc99ae00d5fab41a3865810a14fdcae0e4282`  
		Last Modified: Wed, 24 Jul 2024 02:47:36 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055148e7c7afab8058135dee659557d8317e0666c5684e8d0e735e52fabc027`  
		Last Modified: Wed, 24 Jul 2024 02:47:37 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94905925d83b06832c3322411bd1999be12b101dbfe8783a1466e87542bc9513`  
		Last Modified: Wed, 24 Jul 2024 02:47:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:fd9a194157f2002c6e6f8fbe425be6f2902e8e2b22dbe349436870fd56ff7011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.3 KB (634288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902a26924d810a49b6905ade7804a9d25a6925427880850ea9fe58c881af76ba`

```dockerfile
```

-	Layers:
	-	`sha256:652a64b411c7904d6b084c4510582dc58e7691b52a4fe50e8ab73ef0c5029ebe`  
		Last Modified: Wed, 24 Jul 2024 02:47:36 GMT  
		Size: 588.8 KB (588761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46cfa7a038daf1188c8596fdce8ce75c9630f52715397086ddb190b72c6608d4`  
		Last Modified: Wed, 24 Jul 2024 02:47:36 GMT  
		Size: 45.5 KB (45527 bytes)  
		MIME: application/vnd.in-toto+json
