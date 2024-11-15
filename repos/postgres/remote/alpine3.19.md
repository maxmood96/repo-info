## `postgres:alpine3.19`

```console
$ docker pull postgres@sha256:5a9a1fef919bb8698c7bf758840a13af6e4ed5582efe21243b96e5aa2e8274d3
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

### `postgres:alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:3aa7c3b064ea8ccfcc17f5cf62e8d2d8f7ab6c51a6750b878894d82efdcda003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.2 MB (100192950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:497199803130c0f48a0626152333a6474d61fcbe47726a69f52aff74dc57bb00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:48:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_MAJOR=17
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_VERSION=17.1
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_SHA256=7849db74ef6a8555d0723f87e81539301422fa9c8e9f21cce61fdc14e9199dcd
# Thu, 14 Nov 2024 19:48:01 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:48:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:48:01 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:48:01 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:48:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17937d3d08b4178f319bfcff330dd6506c59fc93fb3689a92412d396389f4d0c`  
		Last Modified: Thu, 14 Nov 2024 21:11:31 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8227a767f0aa033593d4d0a414d8615eef745365bc08b347b1221d821701c2`  
		Last Modified: Thu, 14 Nov 2024 21:11:32 GMT  
		Size: 1.1 MB (1120290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f93ba56e39725f844634e0874b5f0c69e9cd5af24cb17c3d9a8bb12adf0db4`  
		Last Modified: Thu, 14 Nov 2024 21:11:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673d94a55ec98d3e3aba0ef3eb4098d1a4f0d5cfbae0129d5135f1e40c3c653c`  
		Last Modified: Thu, 14 Nov 2024 21:11:35 GMT  
		Size: 95.6 MB (95635762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5192937b481d4004f52b7c6464df779df05987c423f36590f898cfc6d8fc30a4`  
		Last Modified: Thu, 14 Nov 2024 21:11:33 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1e9af10a0f0ddbec51f85f8e5e60371a5ce79e7c8a5d2d50477a58f258d1ec`  
		Last Modified: Thu, 14 Nov 2024 21:11:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752c154e096cf0794c298ab453cf961b9705471aac0cf79d5963158fe47f1084`  
		Last Modified: Thu, 14 Nov 2024 21:11:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85eb7dfec659e44513914da8e4507979bfaf5b8e7ed1debdf038778e730484a`  
		Last Modified: Thu, 14 Nov 2024 21:11:34 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabdea89530bec98815b46411a0000a1defa062424dc29f06e762be7fdc2dd82`  
		Last Modified: Thu, 14 Nov 2024 21:11:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:241172e8b54762fa6f97d504024ffb2e6ba31e92cabdaa6ade4a1eeb6ed079c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1012205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823c6b4d3eff30b0629be4f03849786b74ad61651be9e12f66069459adfaac81`

```dockerfile
```

-	Layers:
	-	`sha256:6717ac783ed8f6412cbb071529ca8d1b9b2b474a581842bacd00fc6fbebb6886`  
		Last Modified: Thu, 14 Nov 2024 21:11:32 GMT  
		Size: 969.3 KB (969309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11137dfdfc911d6ff4004d740b7c6c8f3a8f0af23317444ee91b7b3e25b1dd29`  
		Last Modified: Thu, 14 Nov 2024 21:11:32 GMT  
		Size: 42.9 KB (42896 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:0ddfc75086941fe4f16b7b65de4d98edb518a70894d6c8fab3d6e50ca3bd1571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98531310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7166b43cd2da982a0861a9078372ca73d2a5710a9e248c5ded5350bedec5968b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:48:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_MAJOR=17
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_VERSION=17.1
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_SHA256=7849db74ef6a8555d0723f87e81539301422fa9c8e9f21cce61fdc14e9199dcd
# Thu, 14 Nov 2024 19:48:01 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:48:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:48:01 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:48:01 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:48:01 GMT
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
	-	`sha256:5aa2615eec230123f6a0e89ad8b2756fe04419eb394d6645c8c6d069b10e09b7`  
		Last Modified: Tue, 12 Nov 2024 05:41:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc861194f5cdbcbe7b183cf38c818723d78019d81e754cba744881a41215e67`  
		Last Modified: Thu, 14 Nov 2024 21:14:01 GMT  
		Size: 94.3 MB (94251031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20f32edd98bcc7e21fca5ed3498c2bab15523ea66ce44da34b11a4f7990fbb7`  
		Last Modified: Thu, 14 Nov 2024 21:13:58 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea486d3bba042d8a390578d732297a7a4d9e43b6900ceb4c5a57787e192300c`  
		Last Modified: Thu, 14 Nov 2024 21:13:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252de61c592bc8e35f530a3514a89577d7b72f46ad5968d7bcd41dd56a881a24`  
		Last Modified: Thu, 14 Nov 2024 21:13:57 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cddaae6116453865bcf9e6683801e1dba43f59f6e9328d9141639254f3b345`  
		Last Modified: Thu, 14 Nov 2024 21:13:58 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146fb03c614a434456145e82f5c578cc312984778414a4dff05983ec39df12d2`  
		Last Modified: Thu, 14 Nov 2024 21:13:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:88a09629ff81f0b781eb9912cebd80ad58ee5d05a57134de0df625f16c9753e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 KB (42840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0dd025c37bceb4190ff876c22d4a31fb46befc82cd985a232469cb2f31e2355`

```dockerfile
```

-	Layers:
	-	`sha256:f03b7cc283aaacdbb98d1a14895b8ec628fc3da728d84e96131ad8f433ad436f`  
		Last Modified: Thu, 14 Nov 2024 21:13:57 GMT  
		Size: 42.8 KB (42840 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:b3a7a6051d525dd6d39c1e471469ee882bde4088c0e96a3779c33db454e25db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92814068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a7ea6d65fdc17da27ade3b1361ba430b65d9400849b4add6afbff61d046a70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:48:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_MAJOR=17
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_VERSION=17.1
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_SHA256=7849db74ef6a8555d0723f87e81539301422fa9c8e9f21cce61fdc14e9199dcd
# Thu, 14 Nov 2024 19:48:01 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:48:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:48:01 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:48:01 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:48:01 GMT
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
	-	`sha256:7d724b69202dff14aa464310c973a9df72cd3040855d59315ec350389a2a1ac8`  
		Last Modified: Tue, 12 Nov 2024 11:50:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816db3599afeed2138f9c8909a18bb7d75d79797327d018b8e36fed08fedb0f8`  
		Last Modified: Thu, 14 Nov 2024 21:49:55 GMT  
		Size: 88.8 MB (88782476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001e9bea935fabeecf45549d51ac68d95aec696482793e089a99d8ed9a4eace8`  
		Last Modified: Thu, 14 Nov 2024 21:49:53 GMT  
		Size: 9.9 KB (9885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f31df3c6de68c87f778ffeb202ca4c53e430d843da7b92867c89effc72e3eb1`  
		Last Modified: Thu, 14 Nov 2024 21:49:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b500063858b2576cacb84632f46d5735b5834151ef65a1d4fa7aab0894ca31`  
		Last Modified: Thu, 14 Nov 2024 21:49:53 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2ab7b55fe1905c2e01205c17ebafb0d9afe22258be9a0b8b96f3195df2358f`  
		Last Modified: Thu, 14 Nov 2024 21:49:54 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679bca22e315f194f24fa2f98de1346e2770e532bc8894534802ad4ddf82cf53`  
		Last Modified: Thu, 14 Nov 2024 21:49:54 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:a5d70d3eef4c7b689bd0ddbdc44bfde1c63af6965f01e55874fd39c1a2e20a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1012392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd563bc1a8322d8223fb7dd2b9a374535869bf006a3ca10815f8ebea726d227d`

```dockerfile
```

-	Layers:
	-	`sha256:54118c8c18085cb8ba5a3c6ce8f07f5dfd37a85ba9b1022bdd3564360f86fe91`  
		Last Modified: Thu, 14 Nov 2024 21:49:53 GMT  
		Size: 969.3 KB (969337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c685be52ef4de49eeec23e36b9ae9a6e57cf3f8231720034a29044cf5bdc0e`  
		Last Modified: Thu, 14 Nov 2024 21:49:53 GMT  
		Size: 43.1 KB (43055 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:87c17d7fbc568735f21d465ca402735a000eeae4745f19978a5e6f87ea3c606b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98774826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbd91a10d3824741bcf2ae740dbd7b2ec6d6757fdff0eef29a4e83908d544f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:48:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_MAJOR=17
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_VERSION=17.1
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_SHA256=7849db74ef6a8555d0723f87e81539301422fa9c8e9f21cce61fdc14e9199dcd
# Thu, 14 Nov 2024 19:48:01 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:48:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:48:01 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:48:01 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:48:01 GMT
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
	-	`sha256:8b5cb152d93629bc0c1cb37f6de5a369c7744581cd6166bb4dd478f70b363045`  
		Last Modified: Tue, 12 Nov 2024 09:17:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe8138a2bc94074978765d7efbb2809331dc45a1507e857e2d8a600c29ebd9d`  
		Last Modified: Thu, 14 Nov 2024 21:14:25 GMT  
		Size: 94.3 MB (94349048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf167f159d1c5dbfea1ffaadc2643928ad0c4b9344046971b3758f8ed93d4b06`  
		Last Modified: Thu, 14 Nov 2024 21:14:21 GMT  
		Size: 9.9 KB (9885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5eeec4a89c3ffc8b4614881105503922f45ef7001dd88e5520538fa7c76846b`  
		Last Modified: Thu, 14 Nov 2024 21:14:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91f2f47ada7bed506a5a3c069325ae09ea88541291cc273c1b425e3cb4c29c4`  
		Last Modified: Thu, 14 Nov 2024 21:14:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc0c5c3506a00e5e39f35854bdad378e0cfc94961791bc3ad81624790410bc3`  
		Last Modified: Thu, 14 Nov 2024 21:14:22 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d221f7365312691a30afaa4c34aca268b3346b98822bc301e19b407d9612eb`  
		Last Modified: Thu, 14 Nov 2024 21:14:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:1f0a7cd942d31af6c5daef11239735491cff5c3d3b3a8ca9cb1e980b085c9bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1012446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fda9ca3d15af1f03c48d7fde62a9c741e9e2fcf63a55b1c0b2c7348a9e16822`

```dockerfile
```

-	Layers:
	-	`sha256:8101bb0e93a9a909afba02290c9e76291aa612fa9a41c7de00d8b3beae749b7b`  
		Last Modified: Thu, 14 Nov 2024 21:14:22 GMT  
		Size: 969.4 KB (969353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e508900fb4c693f8a5d05b6dfcb931c265b9a9ebea9ab233b334e6368b602460`  
		Last Modified: Thu, 14 Nov 2024 21:14:21 GMT  
		Size: 43.1 KB (43093 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:be0a5fe96766def4511cb4bc0287b3156116d0e95b1bfdda8206a6dd8215428b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105342824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d667cb94ed7bf5ab1c1cfa552905dba73c332060e2f76c333b48d1093ad0a4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:48:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_MAJOR=17
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_VERSION=17.1
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_SHA256=7849db74ef6a8555d0723f87e81539301422fa9c8e9f21cce61fdc14e9199dcd
# Thu, 14 Nov 2024 19:48:01 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:48:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:48:01 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:48:01 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:48:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35adfdce05677ae32a2184c7b69839c2a2775b69dccbcc9a629ae4458d70b2eb`  
		Last Modified: Thu, 14 Nov 2024 21:11:26 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83a8d183fb074290afd0ad069d6236f1b801e9a7b1e0b3c7c512ca2fa68b994`  
		Last Modified: Thu, 14 Nov 2024 21:12:04 GMT  
		Size: 1.1 MB (1095474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f93ba56e39725f844634e0874b5f0c69e9cd5af24cb17c3d9a8bb12adf0db4`  
		Last Modified: Thu, 14 Nov 2024 21:11:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2f4a096eee92cfc80f5c5d20df6d18cf7110e3e3897313f2e1b9ec2fce3a50`  
		Last Modified: Thu, 14 Nov 2024 21:12:06 GMT  
		Size: 101.0 MB (100976517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235bdf4e2647f19020ec433426fd601139c2e6559bf776494167a5a4664e101d`  
		Last Modified: Thu, 14 Nov 2024 21:12:04 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8c64868d615cb41f2daf5216dafc719f64b73f419110bc883888628eed25cb`  
		Last Modified: Thu, 14 Nov 2024 21:12:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10bc7af4a677329405abc279b9cf574a50b5e909afc2b14e7502ec8f40396e1`  
		Last Modified: Thu, 14 Nov 2024 21:12:05 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1c8848ac3482e3fa4501cdc2a4d7c8073914afa9766110849c792f1bce4661`  
		Last Modified: Thu, 14 Nov 2024 21:12:05 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd76224c94a7c6606ba4e10e6f98b525075f49569db2d13c0c2f40eaa04e062`  
		Last Modified: Thu, 14 Nov 2024 21:12:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:fe8ac1c47e8aef6dca4378a4212f51ad61aa9f4c5aa27ba1dfcfb403c1025e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1012150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83236dc0cbd42d6eafda9109198c05acdb135cbb3236c3f039b79381c63a6fcf`

```dockerfile
```

-	Layers:
	-	`sha256:75e41884b89d3bff9035eaad5021180375a8d068263f7f45cb427de424cae9ce`  
		Last Modified: Thu, 14 Nov 2024 21:12:04 GMT  
		Size: 969.3 KB (969289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd1a93d12ec79252bbc71dc45e31f321daeb10f51e5241c3e94387cdb888cb8`  
		Last Modified: Thu, 14 Nov 2024 21:12:03 GMT  
		Size: 42.9 KB (42861 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:ce151531b061fe0a3d1e48df2f9c72ad992e23f2acd7319cdfcb1446d81d6ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104685110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d009a2166e03e01f9c71b395df070561d85f6bb969ed1e9eff654fa19808689`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:48:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_MAJOR=17
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_VERSION=17.1
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_SHA256=7849db74ef6a8555d0723f87e81539301422fa9c8e9f21cce61fdc14e9199dcd
# Thu, 14 Nov 2024 19:48:01 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:48:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:48:01 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:48:01 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:48:01 GMT
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
	-	`sha256:1a9c8a3c406978e167a2ce8783167ab531948c0e6a0f1ada877f0764a536e708`  
		Last Modified: Tue, 12 Nov 2024 07:04:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6690919c5cb0e46c545aed109896f57c8aeba2c26a2f3337d34ca955b435e7`  
		Last Modified: Thu, 14 Nov 2024 21:15:40 GMT  
		Size: 100.3 MB (100263737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33738c73e86eabb475089d61b3a79535591e40ff12c4090d63cbd8ad34f83e7`  
		Last Modified: Thu, 14 Nov 2024 21:15:37 GMT  
		Size: 9.9 KB (9888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607868f4e4478968c3e95cf747da363705007d7e852b8a3e8ffa059d87f57646`  
		Last Modified: Thu, 14 Nov 2024 21:15:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f2dff5bf7a236ee64400f2c6cdd2c02e9cb731e1e6755d6bb0725550be437e`  
		Last Modified: Thu, 14 Nov 2024 21:15:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a771744fe0105a749c0dacec8235479ad396c8d0f88bcc2ca64bd6d68b0b2900`  
		Last Modified: Thu, 14 Nov 2024 21:15:38 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c80ec785cf9c93154723b388db6e1bfad075e29da0d79829263c8c72029e90`  
		Last Modified: Thu, 14 Nov 2024 21:15:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:cc1beb1d49ca7776a6a10337c6285cd8787316d2e29c0c2a6fc5729d44662087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1008673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47909be1549b00e47098dc3bf228bb4978ef2d765c90a63b874d1c7f717af8d3`

```dockerfile
```

-	Layers:
	-	`sha256:7e688f325e759aa12bb67fc93e25370cefcbf9a2c4ddef7de9b7fbe5b3a58004`  
		Last Modified: Thu, 14 Nov 2024 21:15:37 GMT  
		Size: 965.7 KB (965719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:362f2d209578b476fb83afe88acccb8ba08a203570630e7f15f81e70e6c26637`  
		Last Modified: Thu, 14 Nov 2024 21:15:37 GMT  
		Size: 43.0 KB (42954 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:5d1b8d562470b7733e5b21d037954792166999ffd4da8b272504429c69876785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.9 MB (108852128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893e6fd580ba24804c5ac0eb626e990e002b1fe63efc69322f0416a394695312`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:48:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_MAJOR=17
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_VERSION=17.1
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_SHA256=7849db74ef6a8555d0723f87e81539301422fa9c8e9f21cce61fdc14e9199dcd
# Thu, 14 Nov 2024 19:48:01 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:48:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:48:01 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:48:01 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:48:01 GMT
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
	-	`sha256:7812d75d98e27ac280ac6098ba2faa87afa5ac62c3535dab3584f78baff17305`  
		Last Modified: Tue, 12 Nov 2024 07:39:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf2884195bf328b4adb0be9de3c8bd4e8422a1f2a42af204aa29b97a5113b3a`  
		Last Modified: Thu, 14 Nov 2024 21:18:05 GMT  
		Size: 104.5 MB (104497650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7965e472ae9009fce2a6406911ce3d733aab4a7c9df574bb7f75d76a278518`  
		Last Modified: Thu, 14 Nov 2024 21:18:01 GMT  
		Size: 9.9 KB (9887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca82497bf0e4773846c39bcd2601cf67562c6347a21598fae5bdca3d99d00d0`  
		Last Modified: Thu, 14 Nov 2024 21:18:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01313b52487bf9e636e7dab553008a3c6c75b5cce076d40abba24a2307e4eae4`  
		Last Modified: Thu, 14 Nov 2024 21:18:01 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddca230cb920d93d207f680352efdae620c79a7d0ca4a66e8c4c654933810833`  
		Last Modified: Thu, 14 Nov 2024 21:18:02 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9843f047b8a92f69d969d897c02f3f7a4f675febcb663c7eb3792a508513cf18`  
		Last Modified: Thu, 14 Nov 2024 21:18:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:7e1013f8f688ef9975badbdbe4fdfa965e91ad1dc06bee31db3dc1489f629f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7128282c2267bdfadda4e6713069cb5b86f7782dcdcb85c0db5ff45cfdcba5`

```dockerfile
```

-	Layers:
	-	`sha256:ecc5878d73ce3c81f5c335741d5c7816349ae2079fdabac182bc51648da48901`  
		Last Modified: Thu, 14 Nov 2024 21:18:00 GMT  
		Size: 967.4 KB (967355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d3c4ab771df594661ad1b3fa25390007638415ecb10b86621abf2a2aba8bfbc`  
		Last Modified: Thu, 14 Nov 2024 21:18:00 GMT  
		Size: 42.9 KB (42902 bytes)  
		MIME: application/vnd.in-toto+json
