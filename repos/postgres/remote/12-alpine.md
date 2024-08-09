## `postgres:12-alpine`

```console
$ docker pull postgres@sha256:b9ac6c4c192cd0959ad1195668ac6a3693a7f39c61ca2695868a402707466eda
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
$ docker pull postgres@sha256:9581b2785945245cd55f7122bf2a7eba6998fc60179056120f0e3f9486294284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93152231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f04584d54ccb334bafb5ef4fccbe0ef6a2916b7996523477a8be72bed8a8f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_SHA256=2d543af3009fec7fd5af35f7a70c95085d3eef6b508e517aa9493e99b15e9ea9
# Thu, 08 Aug 2024 16:22:52 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7006ca4e5ceb4b44f99f06accb9d9c5a4852c5ae19517a088fadcbcb56a3baea`  
		Last Modified: Thu, 08 Aug 2024 19:05:16 GMT  
		Size: 987.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6301a8b077cccd7759d9579ba37fa7984627301a5a7c3174dad12dcb889ae03`  
		Last Modified: Thu, 08 Aug 2024 19:05:16 GMT  
		Size: 1.1 MB (1119774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccd4e80f8daf05747edc36996913a25f9bb938758523bb8ed34cea369c1a03c`  
		Last Modified: Thu, 08 Aug 2024 19:05:16 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f481324fa2ffc711a4e014b7ca902abed07722d48250429c6905b339699911`  
		Last Modified: Thu, 08 Aug 2024 19:01:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dd1645f28a7455de9fb657297425c358f658246f5c2c580b1659fc258273de`  
		Last Modified: Thu, 08 Aug 2024 19:05:17 GMT  
		Size: 88.4 MB (88393697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66e3abe31c355c298c2f4685912f1e644b2013ff2aa8658d8b164b588c2aed6`  
		Last Modified: Thu, 08 Aug 2024 19:05:16 GMT  
		Size: 8.7 KB (8685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a7e4811a57380183ec20bbc6a95880c7f225da5d49e4ab19617173a3efb61a`  
		Last Modified: Thu, 08 Aug 2024 19:05:16 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0737b1e05ab16b31ac19c362e53a8badcc5d7615792411bd3667e986b982db8b`  
		Last Modified: Thu, 08 Aug 2024 19:05:17 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2de61ca13987fb082c6c9b969e81cf382d4c1598480f9121ed4b2804441c126`  
		Last Modified: Thu, 08 Aug 2024 19:05:17 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642cab16df749ae50f9f8182bac21eccd008f95f585c34d4470108d82c75f372`  
		Last Modified: Thu, 08 Aug 2024 19:05:17 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:3c156b410e4ac05cf0ffa746324839565f0078b0edab43f7a0d31500f35fbba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.9 KB (632874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072adec9aff8d03c6a0180b0f1734e7dd2b3f292896df592a439d4db3621ac84`

```dockerfile
```

-	Layers:
	-	`sha256:bb9cad641735d9a30e1121092e1eb0cd0c71732ed4784ecd3a0de6168ba32f20`  
		Last Modified: Thu, 08 Aug 2024 19:05:16 GMT  
		Size: 587.8 KB (587755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:442e177abd9a1a52d230129953833d0727124412aed45eb70d926dc7ab851146`  
		Last Modified: Thu, 08 Aug 2024 19:05:16 GMT  
		Size: 45.1 KB (45119 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:0387ef03b4378eede222721133c1f738d553247a8c8b4e3f0dfc783c0b087c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92037108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0aa14d9c8b965c15bf8fb764e14d946a974ba3fab98fbbca48dafd838996804`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_SHA256=2d543af3009fec7fd5af35f7a70c95085d3eef6b508e517aa9493e99b15e9ea9
# Thu, 08 Aug 2024 16:22:52 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25307227c90bae58c84dab41277d5472d9cd00151c62baab3eec8f0811c54942`  
		Last Modified: Thu, 08 Aug 2024 19:06:01 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6ad02c3e211165e47b37a87649b86bd72f65170d27f581321a4650a888cdf9`  
		Last Modified: Thu, 08 Aug 2024 19:06:02 GMT  
		Size: 1.1 MB (1086466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a94a1e71a5af12858f43c42aa95968453af5c4d908ef9ce1368539e6896a2e`  
		Last Modified: Thu, 08 Aug 2024 19:14:08 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a662cefb5c901350ba8f3c6440f7d6cf1d9c7e5dddef2ecd6bbc6cda74b224df`  
		Last Modified: Thu, 08 Aug 2024 19:14:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae61c68e6e57fa535a8a7074c46bfe32a9358122c1308e812fc7d7c62f6be1a`  
		Last Modified: Thu, 08 Aug 2024 19:43:21 GMT  
		Size: 87.6 MB (87569592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa63fb0f98c0b0020626597e1ea411185c454db239f1da76a4c8c94a847f093`  
		Last Modified: Thu, 08 Aug 2024 19:43:19 GMT  
		Size: 8.7 KB (8686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17d2076919025d4d538a186bd7219a8a251e9cf2876123fbe76b43e3e5bfa69`  
		Last Modified: Thu, 08 Aug 2024 19:43:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b097bf935999e9be1bd9ebc4b5d768906e7a54075d28d210dac8df9374e5f5`  
		Last Modified: Thu, 08 Aug 2024 19:43:19 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6102ca29c4bff820d4bf2138defe2bb3e0006678f458cf1bfee9946c5833be89`  
		Last Modified: Thu, 08 Aug 2024 19:43:19 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c3c0fa3eb7db0c0b7bbbf50d42019e5409f098cab0dfb11097e6dacc14d9c1`  
		Last Modified: Thu, 08 Aug 2024 19:43:20 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:8a7ab8ff2d909d5daa14f87e6664e2285a29c9d5ff7c0785e40dbd91fc495048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 KB (45074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45eb3244e4c8d7365dea94d70a1a512b0978f4f224c0bbef246a5b96055fe65b`

```dockerfile
```

-	Layers:
	-	`sha256:56aacac4ba7d5830231d0e005d896bb4f05065aedc45c290a9a3f257d498534d`  
		Last Modified: Thu, 08 Aug 2024 19:43:18 GMT  
		Size: 45.1 KB (45074 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:820eb33795263660eba668a161b5d3f6c7ab9eeeaba1ff2570dada0dde8d8b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86529946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82414c11a3eee57eb8ffca40f1f94ac52e8379b14f3a0f5e4d73c91354ae2ca7`
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
ENV PG_MAJOR=12
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=12.19
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=617e3de52c22e822f4f57d01d5b2240503e198a9eccaf598a851109bd18e6fbb
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:54580e13b5d380a26b24e62a08c1847c1413ece70a758c87a59c5faac9b18d87`  
		Last Modified: Wed, 24 Jul 2024 06:37:12 GMT  
		Size: 82.3 MB (82332651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204f569eb5a4320f4b8290c2b43e553acecb758289d248efc9eb1e0eeed06094`  
		Last Modified: Wed, 24 Jul 2024 06:37:10 GMT  
		Size: 8.7 KB (8687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de91d72673f0caf4924df4081f97ce24cd585163b72bd2ff94ef45cd908b37d2`  
		Last Modified: Wed, 24 Jul 2024 06:37:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb329d2d0b281feb13038d18d8a91fab3f43444ce8ffd131bd4760b7be09a61`  
		Last Modified: Wed, 24 Jul 2024 06:37:10 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eee917ce772beac9e2aa53915bbfe58d459ac5c3aae2dc95c747e57268baee`  
		Last Modified: Wed, 24 Jul 2024 06:37:11 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95a90cd1b1c0947224703309f8ac6fc342abb4a59a3803dffffca102b9f47a6`  
		Last Modified: Wed, 24 Jul 2024 06:37:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:0e75c325ebcd87f90c76b93fdb238718ef4f819968d5cb3ca9dec2eb1dfb4b91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.9 KB (632913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced026cc45a19f5b912acd37c0b55a9afd87dc20362a299afb70a56237772076`

```dockerfile
```

-	Layers:
	-	`sha256:702f48bd0e8a57a5a811fb95c8fe8762bd0e8db9bfdbbc663cf65004543e8d53`  
		Last Modified: Wed, 24 Jul 2024 06:37:10 GMT  
		Size: 587.8 KB (587809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5a6c3205dc0a6efb524fdfa3a5906ee3f195516061a46a20c371de372890b66`  
		Last Modified: Wed, 24 Jul 2024 06:37:10 GMT  
		Size: 45.1 KB (45104 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:586f4f42c6057e4efce7e5952ca5b260244991cad5fd49969f5da0c8654a066d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92464108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df578bb7bc8d6ec8e13483bc64e5dda681ce020851743da0edbd26de3eb58800`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_SHA256=2d543af3009fec7fd5af35f7a70c95085d3eef6b508e517aa9493e99b15e9ea9
# Thu, 08 Aug 2024 16:22:52 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6128292d5cec813248e3e1bf41197e2e1b572046b0574e5dbb3d1c70445350d6`  
		Last Modified: Thu, 08 Aug 2024 19:15:44 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ce109d9333911b16cccda82566ba394f64d3c677ede2a34b7ab42f16ab41ac`  
		Last Modified: Thu, 08 Aug 2024 19:15:45 GMT  
		Size: 1.0 MB (1047247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8719b5d6e156be6f84623d3cd349dc9678b19f21667efefd61252bb423999a`  
		Last Modified: Thu, 08 Aug 2024 19:23:51 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2626fd16b8881a00a560154951ff29f526903a3fea50e65673a9a34ad93097c`  
		Last Modified: Thu, 08 Aug 2024 19:23:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988282d4cc696b68cdec3ff2cc7d7ba271f7b2d7833f11e3ca499d971ccda9d4`  
		Last Modified: Thu, 08 Aug 2024 20:03:52 GMT  
		Size: 87.3 MB (87314072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1698abc1c97d66257e4564390a6e8f8062cdf3c14e81ae442f0357b25838e057`  
		Last Modified: Thu, 08 Aug 2024 20:03:49 GMT  
		Size: 8.7 KB (8684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9266cb286ecffc79ee9cc3a8d7ec059952d2d8f0a801ffa79731512abbddc430`  
		Last Modified: Thu, 08 Aug 2024 20:03:49 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb17a2a13620198ad271b321b893e7388b2dda8b5632ef614b8a76587b40f328`  
		Last Modified: Thu, 08 Aug 2024 20:03:49 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c7e95abc3458de962f0f0dfb47d4c3da36363e0cfa79228b868facd06c8d81`  
		Last Modified: Thu, 08 Aug 2024 20:03:50 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9588a38b83af9c670334ccb079a4d38e43135758b82aced6c5cb236f65bef7ad`  
		Last Modified: Thu, 08 Aug 2024 20:03:50 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:02cc2876add025650001f98b38a2add809870f15fa79db255e1085ea5d4292b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.2 KB (633229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0474cb71447966d96372e8a12e7eca6ad18542b6855e497fd79da637fb585a1`

```dockerfile
```

-	Layers:
	-	`sha256:9d1ef73add8df73446a537f2887e5748927e019e3f21f67bc60c0d82835f1407`  
		Last Modified: Thu, 08 Aug 2024 20:03:49 GMT  
		Size: 587.8 KB (587811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c78e5363572623f3d16140eb50a6a57bb12d46daf1118fd1a80bced963ab799`  
		Last Modified: Thu, 08 Aug 2024 20:03:49 GMT  
		Size: 45.4 KB (45418 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; 386

```console
$ docker pull postgres@sha256:26ca9c675350d6ffd16b39a3ee955082dde8c87b984c3aa6fc87c5bc9632045f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98400016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf1a0e1e68f74da07efed0b4998225eb9cf74e0afb4977bc8ef871401ef09d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:38:29 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Mon, 22 Jul 2024 21:38:30 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_SHA256=2d543af3009fec7fd5af35f7a70c95085d3eef6b508e517aa9493e99b15e9ea9
# Thu, 08 Aug 2024 16:22:52 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3102edabf788d5a2b78bf86bf38811e7a1301ace6f9f6873139731ed1fd67fd2`  
		Last Modified: Thu, 08 Aug 2024 19:08:13 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815181937efb4abb19d5efd00d2786dd0ef7582a0d8e539ce4f8f67c04d707dc`  
		Last Modified: Thu, 08 Aug 2024 19:08:13 GMT  
		Size: 1.1 MB (1094867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9daf0dc7018e63209de4ae4b8ba4ecb392b07e98f0e3b6948b9e80338e888cc`  
		Last Modified: Thu, 08 Aug 2024 19:08:13 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7548c735b3853d42f5f7d012e8e38efc657f1fdf9ac13ee7dce30d6ff57802cb`  
		Last Modified: Thu, 08 Aug 2024 19:08:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7703882b49369f38bc60a262f7a4edd7542a5e03fa0730623f41865876e99c28`  
		Last Modified: Thu, 08 Aug 2024 19:08:16 GMT  
		Size: 93.8 MB (93821217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4976eda02ea6c4306aa4c7db3f1c3539b6636409df9e926af58ab9bcb1c38c54`  
		Last Modified: Thu, 08 Aug 2024 19:08:14 GMT  
		Size: 8.7 KB (8684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec23ae3e116c35c7af76ae21fe5d90514cf6e03a2a246725c0fe8974bf032e6a`  
		Last Modified: Thu, 08 Aug 2024 19:08:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efb49a7394b388c2309709eb51d14ebe4da57807cf7b59125ddbfdf4c5a1643`  
		Last Modified: Thu, 08 Aug 2024 19:08:14 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01de98b6db987fa277239fa3f29da17641d92c3995fd833b2e3df381b5e1afa`  
		Last Modified: Thu, 08 Aug 2024 19:08:15 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e54eb6b4a3ac4ca841e4482b5a120f76e3aba41c68c9cda804160df8462eb1`  
		Last Modified: Thu, 08 Aug 2024 19:08:14 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:f638a8ed2b2a971d26ce5226c830a8f2f30bc5715233fbb3352654d9d15f123d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.8 KB (632804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e8b213cf8fb3b33e6e89be9315148dec3c55f1e4d5fcfb3af4b4634149b977`

```dockerfile
```

-	Layers:
	-	`sha256:0f89c715f5a03dac4a42aa12a2618c1907c244171492bae664cf94105bb7ffef`  
		Last Modified: Thu, 08 Aug 2024 19:08:13 GMT  
		Size: 587.7 KB (587730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8924eb2a1ff4539def14d1bd0ac1b0bacd9542924ec275f043ab326392ffb6cf`  
		Last Modified: Thu, 08 Aug 2024 19:08:13 GMT  
		Size: 45.1 KB (45074 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:270897c17e6db1ea063d0483683a5c4e78c171d2f21cc04fa3081813f475f69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97549191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7d98c1cba2bbc2fd175d6737aac72cdddcdf4d7170f971e0c12cec7d763d7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_SHA256=2d543af3009fec7fd5af35f7a70c95085d3eef6b508e517aa9493e99b15e9ea9
# Thu, 08 Aug 2024 16:22:52 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e6c981040920e1a386b32b0a4e13ee3ff47730a97cf3757106fe4d89dbb695`  
		Last Modified: Thu, 08 Aug 2024 19:27:17 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493d303f50c68c053ed606838d40534d57ffcce8a3fdd2e797fafe2055618b55`  
		Last Modified: Thu, 08 Aug 2024 19:27:18 GMT  
		Size: 1.0 MB (1037926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3aa90b6d475919cb7aa75508f6c1b40b8038a73a82eb4820284623c67297aeb`  
		Last Modified: Thu, 08 Aug 2024 19:37:24 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12063f1d5d8248dcf94c90d709869cce1b3a599082f59b53dafa604d98dbe0b5`  
		Last Modified: Thu, 08 Aug 2024 19:37:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2006a1d5c407208bdad8b9b801daffffd536177931bcad40e0f8b8ee6f5daebb`  
		Last Modified: Thu, 08 Aug 2024 20:16:12 GMT  
		Size: 92.9 MB (92923844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53629fd643c26afda0c7098826e1d4445f90d6eb1cf42c91997c2bc33e54d955`  
		Last Modified: Thu, 08 Aug 2024 20:16:09 GMT  
		Size: 8.7 KB (8687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca419d7b4e52fb95d52dc1009c736da0dc50ea6da591fae74302518f4d8b8840`  
		Last Modified: Thu, 08 Aug 2024 20:16:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bd3e5b2164e056997134104897131c40a155b70926a069ca0543cfb5d873bb`  
		Last Modified: Thu, 08 Aug 2024 20:16:09 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f2de5a2986113ed785ed16bcd7f7b1bc36cffa594bb88717c87dd6a340c578`  
		Last Modified: Thu, 08 Aug 2024 20:16:10 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560fa3ee9000c4570fcbbbc422477cdd49b03014eaf61011ea9d2a3a7812b19a`  
		Last Modified: Thu, 08 Aug 2024 20:16:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:7a58d526a4c00b7f4b52895e3601063c609d8ac52ffd0fe7bdf3de612c8cef85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.3 KB (629344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b624b27f1c13f41de6016c854466abd4f4e835d5af711683a36fc518be9ed42`

```dockerfile
```

-	Layers:
	-	`sha256:78b80d6e6ef2304ed4f30a6ddfa1eaf0f97322b18a426354be6dac3d542e1a69`  
		Last Modified: Thu, 08 Aug 2024 20:16:09 GMT  
		Size: 584.2 KB (584171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd5881fde2bd5d1256390956eced277caaf8d11ae602da6af8263197e158eb9b`  
		Last Modified: Thu, 08 Aug 2024 20:16:09 GMT  
		Size: 45.2 KB (45173 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:622f660430f01699e0ff690029ad935e31e8f425a2bfa07c6530f61aa835def2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93297799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ede3d7404cb48c34ce3363f065aa3eb6f14a9889f004e22ee55b3b9288d559`
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
ENV PG_MAJOR=12
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=12.19
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=617e3de52c22e822f4f57d01d5b2240503e198a9eccaf598a851109bd18e6fbb
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:3350bffce09b74b36774091956f8536b992a1ced54f86615a0e36196a1ba0207`  
		Last Modified: Wed, 24 Jul 2024 01:15:28 GMT  
		Size: 88.8 MB (88823307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc557b0be46fb8a19c379e8018c548cac1b0f433494d612ce8a9207213e6baa`  
		Last Modified: Wed, 24 Jul 2024 01:15:16 GMT  
		Size: 8.7 KB (8687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240611cea37d07462cd449b1c179ad661c41d788c11dc5f35bc69a9141882dcc`  
		Last Modified: Wed, 24 Jul 2024 01:15:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038bca75fbb38d4f87d148f406a853b0a617fe199e461ec09805980611fe109e`  
		Last Modified: Wed, 24 Jul 2024 01:15:16 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c29acb02a802fab2dbfb3fb509b12f5513b2e83f916b96ec55d15630798cb03`  
		Last Modified: Wed, 24 Jul 2024 01:15:17 GMT  
		Size: 5.4 KB (5425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b0cb43b276e7c33291f65bc0bbbd15a701c3a90e3f7ce25b76c3c34e5407db`  
		Last Modified: Wed, 24 Jul 2024 01:15:17 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:a856ca363a927b5ab8abc69f457bbf935cdb86fa82897061ae6d9c13c292ef3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.8 KB (630833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab2442ca1caa7c0aaf457590a5000ef3e4cf9c2837669df0ad88819786819c1`

```dockerfile
```

-	Layers:
	-	`sha256:c9593b44598b9f6ea052988bf75a529306607ded93613e98c8fa9ca5708a06e4`  
		Last Modified: Wed, 24 Jul 2024 01:15:16 GMT  
		Size: 585.8 KB (585849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ca5728e377cc99b95025219054d13051a4add298395aa6403ade2956eb0cee`  
		Last Modified: Wed, 24 Jul 2024 01:15:15 GMT  
		Size: 45.0 KB (44984 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:798e5418452e777e45fdd7dc0a8e1d72c19f481fce22cfc027daf1e9e75c040c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101878158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7b3557323c330e51d4889d3b7d3bb3a6577f338f75ce5db8f65086bb30f26f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_SHA256=2d543af3009fec7fd5af35f7a70c95085d3eef6b508e517aa9493e99b15e9ea9
# Thu, 08 Aug 2024 16:22:52 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acc84b0240620d268a9a34d9656893521b535e5695de2ecd3563889b2a4d089`  
		Last Modified: Thu, 08 Aug 2024 19:24:28 GMT  
		Size: 988.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93655a24699b012088518a937673bedaf8bb107d24b97484b2e34e87e39b6ca9`  
		Last Modified: Thu, 08 Aug 2024 19:24:28 GMT  
		Size: 1.1 MB (1083302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04af72244755ff0ee69184ccc333af9ab88631e9ac7ac522b48ca3084e2e610`  
		Last Modified: Thu, 08 Aug 2024 19:51:03 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4a9eb71a635e22a0c8acdc6fb1c625c7a31f4a6220312f88740ced858bfafd`  
		Last Modified: Thu, 08 Aug 2024 19:51:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff024610b1c7db3486845de058552119ac45a8c3ca501de769179ec20824b9d0`  
		Last Modified: Thu, 08 Aug 2024 20:47:25 GMT  
		Size: 97.3 MB (97317912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8193e1b79f36f31d82e0441e280541ab449b256027879596d08f2f62de0948`  
		Last Modified: Thu, 08 Aug 2024 20:47:23 GMT  
		Size: 8.7 KB (8693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0be33bf86222ac6b15f813703876b122519291521bbe13aa66d9a5518ca4a3`  
		Last Modified: Thu, 08 Aug 2024 20:47:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85262e1d2ba4b8c404804384d6eef5ac86d3348c950cbce8f476c4ca52ac4d4f`  
		Last Modified: Thu, 08 Aug 2024 20:47:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80f5d24498a8fd371d04c7658c45331eb4d3dbc35d8188a1a3ff387c69289e7`  
		Last Modified: Thu, 08 Aug 2024 20:47:24 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb4e4ee38e4fb2fd4303cce66af461aac883d624b4005ff73d8ba6702b53b33`  
		Last Modified: Thu, 08 Aug 2024 20:47:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:ff0cf1e1392854830aa3843797020019005f53e2db17a82029b40177a4dd81a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.9 KB (630920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0a9ef020672a4fcbff49ee80df0af47e08134e5bc9e326be07742b6e349b1b`

```dockerfile
```

-	Layers:
	-	`sha256:94bb9cae5946112176ca5e77116dfc3c157e6c32ccacb91a7b429817815ac54a`  
		Last Modified: Thu, 08 Aug 2024 20:47:23 GMT  
		Size: 585.8 KB (585801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50a8a5e5fefb79ebe610e508a8041adb60e9b2c168ec97d827675e7315b8c6c4`  
		Last Modified: Thu, 08 Aug 2024 20:47:23 GMT  
		Size: 45.1 KB (45119 bytes)  
		MIME: application/vnd.in-toto+json
