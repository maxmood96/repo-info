## `postgres:17-alpine`

```console
$ docker pull postgres@sha256:5e6ebbcc4a10913f7aa9f838d0debe3b84a6fc5bd37962db4e6d4397fb3c5fcf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:17-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:b910575268455ec1748ad35f07349887a526fb90951b16ffda7d634c95231b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98143320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb46dc8bfad7db529491f36c04715a9b63f57af0721563435ab17cdb90f6017f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_SHA256=7e276131c0fdd6b62588dbad9b3bb24b8c3498d5009328dba59af16e819109de
# Thu, 26 Sep 2024 18:19:57 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79abea055734e579d992a6fd175b9383bf48b878213618b71d65d46903980c4`  
		Last Modified: Fri, 27 Sep 2024 00:03:16 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4479bb44c7148bbf2aabf66f32811632ca00b95093fc65c89626dc7da42f55ec`  
		Last Modified: Fri, 27 Sep 2024 00:03:17 GMT  
		Size: 1.1 MB (1119776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470eef99dec753d40d3b9ae592e32c5d1ad0e7daaf6d9e59d176204de264ad5e`  
		Last Modified: Fri, 27 Sep 2024 00:03:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d5e490c51dead93766c1af6ec321bb091fd65db40199fec3d1bdb75919e353`  
		Last Modified: Fri, 27 Sep 2024 00:03:19 GMT  
		Size: 93.4 MB (93382861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f560d2170904dd831f651cf62e529417929dddaa36c5ae48852e263512d7a0d`  
		Last Modified: Fri, 27 Sep 2024 00:03:17 GMT  
		Size: 9.9 KB (9879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c99d4a3f4170f72864b25255b2bd63cd5d5b547c6b4d2ae56d020eada33196`  
		Last Modified: Fri, 27 Sep 2024 00:03:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfdc0509fd5cd6e21fde83d57a2517989a910d075f5dbe0c410b1efe6c7d1cf`  
		Last Modified: Fri, 27 Sep 2024 00:03:18 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e632debb317998b9bacd4044af9841bf5a7a5cdf014f4cd868b3290a88278d10`  
		Last Modified: Fri, 27 Sep 2024 00:03:18 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566f5c6d1a925367f306a2e35aa3718406a3e98f611286c233cb5db006a6747f`  
		Last Modified: Fri, 27 Sep 2024 00:03:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:50adea805d22970d1e89e66293065fd8f1aa7e7e49db53e9761074e4dd31e06b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.9 KB (634933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dbc91e2f5ead2b1f78e203e6efd01f4040283e72124a48635720036873e61f`

```dockerfile
```

-	Layers:
	-	`sha256:3bc8c48209e808351cb52a6b3262624010aa9d03a38b3e5475a220eaa5e59dce`  
		Last Modified: Fri, 27 Sep 2024 00:03:16 GMT  
		Size: 591.3 KB (591322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f921a2eac0ba9442e0b0886438f5ef57381f89958e32e9733a676d2db4d18d5b`  
		Last Modified: Fri, 27 Sep 2024 00:03:17 GMT  
		Size: 43.6 KB (43611 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:7991c58c4cff9a417e83e09a6b069b04b5e215c9a66518c979ca5db7367a9a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96813361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802c680646ecb64bb8342beb3d16e39194c8f7df4f7821015c58e78e861989c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_SHA256=7e276131c0fdd6b62588dbad9b3bb24b8c3498d5009328dba59af16e819109de
# Thu, 26 Sep 2024 18:19:57 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1926ba8f8f62878b68875756f8686ff4fbac12ecedb3040e7fcdb795834f064`  
		Last Modified: Sat, 07 Sep 2024 08:42:22 GMT  
		Size: 982.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8999ec1aa34d37759a1bc9a1ab2364f588fa7168269d15b795fd1f59eb268fb`  
		Last Modified: Sat, 07 Sep 2024 08:42:22 GMT  
		Size: 1.1 MB (1086464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6402e77ba8264a82c2754d3874c4645dcdb1f2ffbb0172587cb2b67059d5e4c`  
		Last Modified: Sat, 07 Sep 2024 08:42:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56e1265ca909a31287d04cc7dc51b8635acacb5794666bb2e2f38cb79528514`  
		Last Modified: Fri, 27 Sep 2024 00:49:46 GMT  
		Size: 92.3 MB (92343507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420f1bf641d6cd954235f74db4164c6f67df063a027884ea795b1ba28f5c37fa`  
		Last Modified: Fri, 27 Sep 2024 00:49:43 GMT  
		Size: 9.9 KB (9885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bdb7f80765a6f43b984fcc5b4b2b5b1fcf6e8b3b1eb63a1dc5c93f7adc8421`  
		Last Modified: Fri, 27 Sep 2024 00:49:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15b8d3fa3bd338d3487314aad72c831023772bc45f2c4ab754038ed9ed45afc`  
		Last Modified: Fri, 27 Sep 2024 00:49:43 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41301be9cd78e60b83d64261721acb985ce896cbfe32957d2621f007db168e1`  
		Last Modified: Fri, 27 Sep 2024 00:49:44 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82974480458d7cc425956f551c5187109e50a376e805a4057c6b521cc64f139e`  
		Last Modified: Fri, 27 Sep 2024 00:49:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:0017c7c7e09ed953327b012343ab0cebcbb1ce9a8504253f8bad520534395d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 KB (43570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8892ea0804b859438028080b4a9eb1e8bbefc9d8cf6c40e8f5f1b9cae9992f67`

```dockerfile
```

-	Layers:
	-	`sha256:a17527b7de103c23354e4e26fddf6c3fd9d62b89976aa702bf0c3d826189bff9`  
		Last Modified: Fri, 27 Sep 2024 00:49:43 GMT  
		Size: 43.6 KB (43570 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; 386

```console
$ docker pull postgres@sha256:6e8e5deb17e6034ce40556dc1bccddd152fcb8cba1085f984b13c4eef135d408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103499018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0c1a3b399b51c0bfa0a4526a9a94a2ed9059231b29d99845002d9609ddcee3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_SHA256=7e276131c0fdd6b62588dbad9b3bb24b8c3498d5009328dba59af16e819109de
# Thu, 26 Sep 2024 18:19:57 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c5679cf6d989e038bec6712d6cc673d40037111ac9d97edff06de324cf602a`  
		Last Modified: Fri, 27 Sep 2024 00:03:59 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c969a5d259af5cb48a36f3685e7fde0c5c4f42c04e5ba500d5e7b5ff2ae438d8`  
		Last Modified: Fri, 27 Sep 2024 00:04:00 GMT  
		Size: 1.1 MB (1094867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f1273db976c75ab8e302ad30e602b40805f2f4ea90c344e86ca6c3e995616f`  
		Last Modified: Fri, 27 Sep 2024 00:03:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aef97e580f49bee7544fd4b4f7ffc91ab65204fbcde821a81d72731c0241dbe`  
		Last Modified: Fri, 27 Sep 2024 00:04:02 GMT  
		Size: 98.9 MB (98918103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9651708d2373420973f0d10895fae033c0db054946a75ab154b33b0bf6de248d`  
		Last Modified: Fri, 27 Sep 2024 00:04:00 GMT  
		Size: 9.9 KB (9882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68345d1792ae76235ef85b04c1c14ca823bc75bab2b5f8e92b8e9ff0ece8ad08`  
		Last Modified: Fri, 27 Sep 2024 00:04:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df1b25a67c671bbb7c255746dcf4f14fb61c3f2ae17b0a84fa68df9a9388a31`  
		Last Modified: Fri, 27 Sep 2024 00:04:01 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2b380c9be6c7f24198f807110f31fade68ee36c6bf17a6dd9f14a6009f7163`  
		Last Modified: Fri, 27 Sep 2024 00:04:01 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714564639bd61fff6032e41201b7502d854bf9e544ae257952818bd73edf626f`  
		Last Modified: Fri, 27 Sep 2024 00:04:01 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:82daca8a2e256bc59850364baefc72d4be4ca3695a334e0a03a86afaca36ed05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.8 KB (634846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d589e760a99c8651e224d44938c1c1a25c41e12daeaca4898358159fd17eb1`

```dockerfile
```

-	Layers:
	-	`sha256:5029123ab9360907e2e5292497c03d79818671b9ec13f43f576ac7aaff755244`  
		Last Modified: Fri, 27 Sep 2024 00:04:00 GMT  
		Size: 591.3 KB (591287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42e9240835e1a5a16a0fc9052fc6f6dd7e44c9c584b58d310bb04d9cba693361`  
		Last Modified: Fri, 27 Sep 2024 00:03:59 GMT  
		Size: 43.6 KB (43559 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:f47da77086172668cf3228f75e8c1d72759c661485b4ce299b5b00c5587d450c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102780556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3a9522b61b5c4106a9ce56bcb9b3daf0e0edbfe5d9e2927e77b283e71cb471`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_SHA256=7e276131c0fdd6b62588dbad9b3bb24b8c3498d5009328dba59af16e819109de
# Thu, 26 Sep 2024 18:19:57 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ce5dee6cde0af5fd1e7e70a7243212613987d185082bd79b6777171ab4de60`  
		Last Modified: Fri, 27 Sep 2024 01:25:01 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05679565b3500ce762c4b9e03900221a32b43df52a3e5bac9141e5eaff0cc27f`  
		Last Modified: Fri, 27 Sep 2024 01:25:02 GMT  
		Size: 1.0 MB (1037927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bb250e7ec3ae93f435e6892ccc1921ef3b11254806eb1270aaa26262e3f8f3`  
		Last Modified: Fri, 27 Sep 2024 01:25:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50425e513775f5d3f00ded3bb5adea6ead5becf846f8aa2c7a0cc09a06b2aa39`  
		Last Modified: Fri, 27 Sep 2024 01:25:05 GMT  
		Size: 98.2 MB (98153328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ce3d44309ac9bcadc5a3dbd4197dbecd7e3dea4006fce5a500a66fbfe13ed8`  
		Last Modified: Fri, 27 Sep 2024 01:25:02 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044b19b01a83202a4096f51834e45f815168ca18a034ac0aac0ee290e5f0791a`  
		Last Modified: Fri, 27 Sep 2024 01:25:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f94a0efa83d0b1eed8f1d32a56113d308f7931956085dfe7a14f7b68af43f5e`  
		Last Modified: Fri, 27 Sep 2024 01:25:03 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94d38d9912f894fdd8ed4656b49f6061bb4d8796aad255d93bcce6cca84f379`  
		Last Modified: Fri, 27 Sep 2024 01:25:03 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565324c8e1db8d78017eb06d51d87c15cb55c996454c19f67c5b3b081fefa2b0`  
		Last Modified: Fri, 27 Sep 2024 01:25:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:d7f0f5eaff3171fa3492aef7ff842547ab9a65e423097d4b0c8b73c840219e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.4 KB (631426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749859318d285b1af63d24e9a10431692cb70f25e1e8f77d4f59a5e8762e3c56`

```dockerfile
```

-	Layers:
	-	`sha256:4e418490d0878acbba68d3720cd002dc9bae3c4e93701d78bdedb6333460351e`  
		Last Modified: Fri, 27 Sep 2024 01:25:02 GMT  
		Size: 587.8 KB (587750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e57ab394ec9872df784baec50c35f420cb5cc98b7a6322d74a062b39c40e0727`  
		Last Modified: Fri, 27 Sep 2024 01:25:02 GMT  
		Size: 43.7 KB (43676 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:5d02992cda32e6be6a7cb07f12ff3258843d770f2c9009d07e5a725e376fcef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107062096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a25a3dda1c8f9991b6579fe63580b535e95d78167f7f3a404aa13914557c7dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_SHA256=7e276131c0fdd6b62588dbad9b3bb24b8c3498d5009328dba59af16e819109de
# Thu, 26 Sep 2024 18:19:57 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8e9c8c4c476878c5a36e1f0f5fd73fe6e458d57f402912d2d9013c690fb7cc`  
		Last Modified: Fri, 27 Sep 2024 00:47:17 GMT  
		Size: 988.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b0f9ee250b51eab07dbbdd6559dda42bcb10f959235396fc551c18af712670`  
		Last Modified: Fri, 27 Sep 2024 00:47:18 GMT  
		Size: 1.1 MB (1083304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f77f9f872574b2ae1c2f304df50dff49ae9b8f3db3701e33656d1281edd322`  
		Last Modified: Fri, 27 Sep 2024 00:47:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f8509ce424841a6f6fda691a18f7cfb466fea90fee1fe2bf7a8e24eba09814`  
		Last Modified: Fri, 27 Sep 2024 00:47:19 GMT  
		Size: 102.5 MB (102500299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80508a8df83d00e4a9c3f197cc3ff0466bd10633463dcb755e45b11a91f95d8`  
		Last Modified: Fri, 27 Sep 2024 00:47:18 GMT  
		Size: 9.9 KB (9887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252c62545fff4582d50b29feff004c59d8a67ee5badc7ac9a334eeabe91e8031`  
		Last Modified: Fri, 27 Sep 2024 00:47:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a51c94f6c88c40607acaa45c16b63cb1aa66463fddeab71b0d1dabd3ecdd81`  
		Last Modified: Fri, 27 Sep 2024 00:47:19 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281ed1c7ab6124a6ea67f68619d1d7c368d51b06124a907604e255d691e50012`  
		Last Modified: Fri, 27 Sep 2024 00:47:19 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb56b8d3efd4da9dbd425dd92058c02b737dea6484ac4b03b90e14afa4bb78a`  
		Last Modified: Fri, 27 Sep 2024 00:47:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:f1314ec86b4fbd3523b6a03a0daba464d6fd31b306abd99f3591db35669e915b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.0 KB (632985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946fd8aa47861afc1f451ed19e34754316c77bb38b70bb2001b85a5eb1375a04`

```dockerfile
```

-	Layers:
	-	`sha256:0bb06eec097b344ca1f9e57cd2e0f81a08a950f932e81516c92eb4192bf02aff`  
		Last Modified: Fri, 27 Sep 2024 00:47:17 GMT  
		Size: 589.4 KB (589368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f5b2fa620440c88eee9bab6ab1fde35496a14fdb477672744704378c9384c06`  
		Last Modified: Fri, 27 Sep 2024 00:47:17 GMT  
		Size: 43.6 KB (43617 bytes)  
		MIME: application/vnd.in-toto+json
