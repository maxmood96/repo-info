## `postgres:17beta2-alpine3.19`

```console
$ docker pull postgres@sha256:c54d61a3d02d7340db641652e640c1d261ab51a62ec8b4a56fbb5579caab4972
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

### `postgres:17beta2-alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:07fe727b280a9ebc35347c90617a07b29410d78659f86c35588f469e4978336f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98107959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84ac2735e858778d8ee8213c36afebe167c25176c5fc32bb08e09401d83d0fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 02 Jul 2024 00:03:06 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17beta2
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_SHA256=157af3af2cbc40364990835f518aea0711703e1c48f204b54dfd49b46cd8716c
# Tue, 02 Jul 2024 00:03:06 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28714b8735546f81995f4ce653d4884aa7e306d135ecef2fcca7eea138d5a07a`  
		Last Modified: Mon, 22 Jul 2024 23:10:38 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90414699547b613f33782d08901620813ed5617dce6b13e9110dfb2a360fd9ca`  
		Last Modified: Mon, 22 Jul 2024 23:10:39 GMT  
		Size: 1.1 MB (1120289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3844f4f40a884ae7c8544651480c336e3bd2c70bd619252f16ecb3b69d1530d0`  
		Last Modified: Mon, 22 Jul 2024 23:10:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9b1b78eca85d9905318cd7b5b35003076d47eedb04fa9b8f4d01387c69b675`  
		Last Modified: Mon, 22 Jul 2024 23:10:40 GMT  
		Size: 93.6 MB (93551468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d1a3c478cf77697a3ad5601bbc6e8a4022fda3f979a8fdbc970db912c5a8c0`  
		Last Modified: Mon, 22 Jul 2024 23:10:39 GMT  
		Size: 9.9 KB (9885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82916f684b84f22e5b757e4ae60d6722d9536d0927ca79e80a40d705e1edc35`  
		Last Modified: Mon, 22 Jul 2024 23:10:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed374864be52bafc7ca9e86056f97414fcab3818ec52adabe8c510ed4842c9f`  
		Last Modified: Mon, 22 Jul 2024 23:10:39 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1321a756253bb9675adfbe4b172aabc180de2c9f751da670520185c62eb73e7e`  
		Last Modified: Mon, 22 Jul 2024 23:10:40 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c73f81dc9b157160ebe69770f080194db4e7eee16bf5d144ea5dbd7348bbfa`  
		Last Modified: Mon, 22 Jul 2024 23:10:40 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:3ade753e54481dcbfc49399d7af35499fa3ec8dfba5e68b596cd66a4a5fc6154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a48053eec6bb2151a2d6bb06cd457a70b70dcc973af258d518c8ea918c04b7`

```dockerfile
```

-	Layers:
	-	`sha256:aac7356f700ec6b678db0841f280ba8d2b3ecd4240ef1ef35a5434457954679a`  
		Last Modified: Mon, 22 Jul 2024 23:10:39 GMT  
		Size: 968.4 KB (968377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36ceb12f24f9a8658d4cbbedea67eba3c77908f226bb614e302bc4bddf6e7aff`  
		Last Modified: Mon, 22 Jul 2024 23:10:39 GMT  
		Size: 41.9 KB (41912 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:ac0b740c865b39743f5a2089aa9b0b37e02e9a3c6440692264e3b05a88e90cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96748525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88129f535244308020a6d581e0c2fb4ce99298d76b6cbb4b89ee9dab34de42f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 02 Jul 2024 00:03:06 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17beta2
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_SHA256=157af3af2cbc40364990835f518aea0711703e1c48f204b54dfd49b46cd8716c
# Tue, 02 Jul 2024 00:03:06 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92db845726b4ef5f8ebe5ba287fd7c32243caf3658933582eec2af1b0f3a7a50`  
		Last Modified: Tue, 23 Jul 2024 07:35:04 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc40a1c8b107e2354a2c6161d4558c68f9ccb273de07130617b20be1864e0e7`  
		Last Modified: Tue, 23 Jul 2024 07:35:04 GMT  
		Size: 1.1 MB (1086685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75ccbf4632584e9faac08f2c87a35d84cc73915f5bbb0d838f01b89e9244fd8`  
		Last Modified: Tue, 23 Jul 2024 07:35:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82febd10507fa63be0b1c5f06848b29ad185239629e222ea25dafa6ec784544`  
		Last Modified: Tue, 23 Jul 2024 07:35:07 GMT  
		Size: 92.5 MB (92469001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8844dd4abe79c4457f8fcb7fe177dc2a7e9bb211b978a9471c1cd3f29ebcb2f`  
		Last Modified: Tue, 23 Jul 2024 07:35:05 GMT  
		Size: 9.9 KB (9887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caef6a2dc48e3048c0146fe462bff1d4b782eb2d6be1532e46d23fd996786312`  
		Last Modified: Tue, 23 Jul 2024 07:35:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597fed88a77e61bfcb501577beedc47b0a9140087638e3792a11d455dc97c208`  
		Last Modified: Tue, 23 Jul 2024 07:35:05 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7598b1365c5d871b489eb1fc8f6de5c515057320a9bad816647065459015c72f`  
		Last Modified: Tue, 23 Jul 2024 07:35:05 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c6a6365d4795f6f4e1715f18ad504b651e3be4be06ca13cae807458d017401`  
		Last Modified: Tue, 23 Jul 2024 07:35:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:0390b13876829ec7c6b80e4d5eac7e55f8079b1d92ee17bbba5ce12d7819c8d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 KB (41831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf5e06747ff879cc92cb26197cea87b64885e6697ce48db03b717d1a733fbf9`

```dockerfile
```

-	Layers:
	-	`sha256:c88e6eea8609d269de1208d85d88085bcf03c03696e88de8e5e8d8489093bf0e`  
		Last Modified: Tue, 23 Jul 2024 07:35:04 GMT  
		Size: 41.8 KB (41831 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:3811c6bc84adedb2ac01518822d77e5d73538634faa2f1a8224c464645cb0d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92780243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:601fcf7f1f4d7140cb6a645270cda6e8de89375fc870792936f878f4a7ec7a8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:32 GMT
ADD file:a79253a22e927307fa2edd1752e7945fd88afbb97c73bbbe771cc99947c0517a in / 
# Thu, 20 Jun 2024 18:00:32 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17beta2
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_SHA256=157af3af2cbc40364990835f518aea0711703e1c48f204b54dfd49b46cd8716c
# Tue, 02 Jul 2024 00:03:06 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4007367bb0cf596fd27d2207989b3864272eb2e5caf7429c07e68abc3bd47b0c`  
		Last Modified: Thu, 20 Jun 2024 18:01:06 GMT  
		Size: 2.9 MB (2926498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19f2931a4a6163e1a9d50856738ec3f9e2b712e5dc14e5d2b097f56dbb2b3c9`  
		Last Modified: Wed, 03 Jul 2024 05:03:04 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85854c39c5a0b16e3f5d4f5a999af697753ebb9bcc47d49aa6b757c3984b136`  
		Last Modified: Wed, 03 Jul 2024 05:03:05 GMT  
		Size: 1.1 MB (1086684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5000205007919fb5dddadb17acf7af974d5255557c9140b18344d98da7aab72f`  
		Last Modified: Wed, 03 Jul 2024 05:03:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f769f8b75a94c7fe0dd71d11f4c4523a3f941c57b5650a177794ed07182c33f7`  
		Last Modified: Wed, 03 Jul 2024 05:03:07 GMT  
		Size: 88.7 MB (88749900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ff8c6cddcd42f758e606bab906c19f0e04fa8fdfaa4234316e2dcf93360052`  
		Last Modified: Wed, 03 Jul 2024 05:03:05 GMT  
		Size: 9.9 KB (9887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c709f9d3a3fdd767b0e38362c8d526100d7a3d28e7f77c2b9de559af8b127206`  
		Last Modified: Wed, 03 Jul 2024 05:03:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dfa390c40f9e076da0eaa7b042b7748886417b01f022bed81d5718a2e0d91c`  
		Last Modified: Wed, 03 Jul 2024 05:03:06 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881ed2f7d41fdd96f0bc80fe3aa7a1e2403f2fdd8dc745909ed16fd6b244c034`  
		Last Modified: Wed, 03 Jul 2024 05:03:06 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35038fe893117d2b1906675fd9d4817217e07afcf5ff40b2d2717379e467df69`  
		Last Modified: Wed, 03 Jul 2024 05:03:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:295ab18de86f57e9af2f5c8f3251e644886da9011288a0dd6b87449e2ad117ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1000.5 KB (1000487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0019be0f36d3167645c1c4111ae323c2c7ec570e4269da08f9238ce533a10dc2`

```dockerfile
```

-	Layers:
	-	`sha256:0e72e50fd2de4cf7f7d7d6d9709e8b54298e0a86517718a77eab506f04e90cf3`  
		Last Modified: Wed, 03 Jul 2024 05:03:05 GMT  
		Size: 958.4 KB (958437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:755f584f42e8c855bead49fe405db983cef433526a8828b653e90d0588230aeb`  
		Last Modified: Wed, 03 Jul 2024 05:03:04 GMT  
		Size: 42.0 KB (42050 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:8bff59a94c4b54990c66c323f3d9d2c05d34d9a7ce72e2b8f238ce8b97e0af60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.7 MB (98733275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27201a893ad9f9d14202fe45017e8d2b90b60e0b4457652e5f7dc7921cf2c76a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17beta2
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_SHA256=157af3af2cbc40364990835f518aea0711703e1c48f204b54dfd49b46cd8716c
# Tue, 02 Jul 2024 00:03:06 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9210757960e70d52baae60756469488b35e26b1b412bd8a17a75bd7973c60f`  
		Last Modified: Wed, 03 Jul 2024 04:02:34 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a75ed235b4437263d6d21b5ad60009fbe573944b55eac89e2423426c1059b0`  
		Last Modified: Wed, 03 Jul 2024 04:02:35 GMT  
		Size: 1.0 MB (1049344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd53803080ad03be8522cd349701fb4775130012007b5b478667a0cc4e84c4a`  
		Last Modified: Wed, 03 Jul 2024 04:02:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d408d5bac3af164279111fa36c76c4b388f774dccb943304c38f289d4df14a`  
		Last Modified: Wed, 03 Jul 2024 04:02:38 GMT  
		Size: 94.3 MB (94309562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0792ec15dc37eb9cb2324d6273a633a00d3fe90b1bd3520e01fb896a3df63d`  
		Last Modified: Wed, 03 Jul 2024 04:02:35 GMT  
		Size: 9.9 KB (9886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a70263906e49dff4de2ef211269fd22df69f818e688085f6894a30cccfd737`  
		Last Modified: Wed, 03 Jul 2024 04:02:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5cacd0bb08a390354d15f6cd7d45bf9deac796822da2cd57c411b94a61e0da`  
		Last Modified: Wed, 03 Jul 2024 04:02:36 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aac1fdf9f05866b0b95b0090f8de7de2b851cae05dfb4afe688b293923d86fd`  
		Last Modified: Wed, 03 Jul 2024 04:02:36 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06926fa5ebb5b5a3babb92df183c34924740a0730395bee2a6913654b622ac2`  
		Last Modified: Wed, 03 Jul 2024 04:02:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:354adba60afa4d171dc417cf541c3bc76b91126f3e820aa8db6f2d372b1e8177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1000.6 KB (1000622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c755c90e7def9eedbc46043af5a4c467d2ab3074ee29a022b4a42efff5580886`

```dockerfile
```

-	Layers:
	-	`sha256:aedef9b6284c496e294aa2eedb8cbcc7d2ed50bd843e1c9a71c52fee9a4ac9e7`  
		Last Modified: Wed, 03 Jul 2024 04:02:35 GMT  
		Size: 958.4 KB (958445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f73c5e3175c47033e5020c70ad8b031ceae5865c3d3b23fd66fa54342d2269c3`  
		Last Modified: Wed, 03 Jul 2024 04:02:34 GMT  
		Size: 42.2 KB (42177 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:73f661bd8af3b219937a1e82967fb8e6c32df07e9b0aef3a1b77ff5116af8c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103408257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37feaf9e826a6f55972b56d30b60d2e3502fb09346b6946a50aa53f2c0c76712`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 02 Jul 2024 00:03:06 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17beta2
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_SHA256=157af3af2cbc40364990835f518aea0711703e1c48f204b54dfd49b46cd8716c
# Tue, 02 Jul 2024 00:03:06 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc3db61feded63ffc85c1358e70b5c5e573b49a3450c9a0d764134ac44e34d8`  
		Last Modified: Mon, 22 Jul 2024 22:15:39 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df353f38c15bbe0471cc2e722c565da69f04f34f007c6b5c15f65b04653f3586`  
		Last Modified: Mon, 22 Jul 2024 22:15:39 GMT  
		Size: 1.1 MB (1095475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986deadef2be15442a2408bcca509b1bfbd5d24df4fec787b1494d35b032f744`  
		Last Modified: Mon, 22 Jul 2024 22:15:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67efe244cc16be5e777dcc51ae7d81a06a9e12f2e1577a85b07d7e5f531c1b63`  
		Last Modified: Mon, 22 Jul 2024 22:15:42 GMT  
		Size: 99.0 MB (99043017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9174247a1236d76334a7aef1b8d93ff91782a78f12ef47dc89de5c624c8735c6`  
		Last Modified: Mon, 22 Jul 2024 22:15:40 GMT  
		Size: 9.9 KB (9886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612b2bbc4ddd20d27e77c6e8f9fd1c6f50150c525e6cccde0054b0c26adbd0ae`  
		Last Modified: Mon, 22 Jul 2024 22:15:40 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61638ec83ad18d53dd76664347db07c0a4113846dadc41154f42a1d52588ebe0`  
		Last Modified: Mon, 22 Jul 2024 22:15:40 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4689dd1d6c36d20ce33c87cf61f7144ae8aea4919bf274613f2018a021ac1a`  
		Last Modified: Mon, 22 Jul 2024 22:15:40 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e295b2559496a90bf31aa2d232581289afeb57418571af3f1afda6c648988c`  
		Last Modified: Mon, 22 Jul 2024 22:15:40 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:e059ad5725165f8ba7abbc6901377bfd7e830cd1fa8f05653df998bc49be3fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1182a3feef33fa5f7d928fd445647389e8789b7c360af6f8a9c1671dc7eeb68b`

```dockerfile
```

-	Layers:
	-	`sha256:2ff9d233bbb66d76f863730216e1613376f5cf97741a190fe9e0e60730bab57e`  
		Last Modified: Mon, 22 Jul 2024 22:15:39 GMT  
		Size: 968.4 KB (968367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa64945ceb59fc2eff19c3232ec726f0d75aad531da7164cb8ba57a7e6e0aee6`  
		Last Modified: Mon, 22 Jul 2024 22:15:39 GMT  
		Size: 41.9 KB (41885 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:0d3c74f45ab7067a584ce7eb99313138bc81e3d2aa7e3452103ee970fe372ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104638045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e207c07179d5d0d60471494b5e976f8ec4365cf6196c5a87299b36a5881e3f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:27 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Thu, 20 Jun 2024 18:18:28 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17beta2
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_SHA256=157af3af2cbc40364990835f518aea0711703e1c48f204b54dfd49b46cd8716c
# Tue, 02 Jul 2024 00:03:06 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a87ce480a1e6b2a211e539793eb8993daec4a7b45a3b284a63476a172be632c2`  
		Last Modified: Thu, 20 Jun 2024 18:19:08 GMT  
		Size: 3.4 MB (3360635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc56364d57172e5c624f0ed3822a701bb1288a412f960f3447409872376e7e7f`  
		Last Modified: Wed, 03 Jul 2024 10:11:53 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dad81f6714d8be04bc8bf1da45c6734167fa3b3622e8f9804892e4fa6310d68`  
		Last Modified: Wed, 03 Jul 2024 10:11:53 GMT  
		Size: 1.0 MB (1039707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd25e6aea2157883a0a2a58d31ffc54437e418e848db3f0a857116f6d3e4e74`  
		Last Modified: Wed, 03 Jul 2024 10:11:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd98ef0107d1a138c1c9b60811d36bbb73f2f6e1a98b98487764a019fefa35b1`  
		Last Modified: Wed, 03 Jul 2024 10:11:56 GMT  
		Size: 100.2 MB (100220531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5884fc3146d05ffce78289c0829ac2ab873b988e56b384774b47bb5d57fe441a`  
		Last Modified: Wed, 03 Jul 2024 10:11:54 GMT  
		Size: 9.9 KB (9892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1621f7b5016f69a3bfb0b0bc652bb1161140fa2b78af54712605e1a9abc4b362`  
		Last Modified: Wed, 03 Jul 2024 10:11:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093eade289c792c342f40c0bf3fd7e67af085b355b525b17e8fd334fd0d14a16`  
		Last Modified: Wed, 03 Jul 2024 10:11:55 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646b509599091e3e25eef45adb081242986fa5aa1e7672bb29f770b2bb0e440c`  
		Last Modified: Wed, 03 Jul 2024 10:11:55 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe01479e161f309ab352c4fead2dc9fd2ecf277fedde71e8c4342dda798fbc6`  
		Last Modified: Wed, 03 Jul 2024 10:11:55 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:2bf8ab2479ae6fa9f852ef10102b451fdc0b8b8518961a9b32bfea943f1db532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **996.9 KB (996918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c3a9235a2906627037f95ed660877f3c1d9df8f85df78bfda9fdafd1a481b8`

```dockerfile
```

-	Layers:
	-	`sha256:f10992d50ddad983bf171fcb32c12ee8d58abef13653d20284b388271d384149`  
		Last Modified: Wed, 03 Jul 2024 10:11:54 GMT  
		Size: 955.0 KB (954966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca39badef3d361a56240a37a921c632c7ba4a440f4a6d7acfc476d22cb00cac7`  
		Last Modified: Wed, 03 Jul 2024 10:11:53 GMT  
		Size: 42.0 KB (41952 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:fd8059e88ac4ce3b82e606c9e949b92746243e790d4de49e01e456c1b5c89c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108814029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927778f8124a4bc27cfcca21e3502ae839a888d007935d859c18e7e71558ddb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:12 GMT
ADD file:4aa205db6913ec3fd53a65bd281586a5f6abde77d41f1ffab554706c04822982 in / 
# Thu, 20 Jun 2024 17:42:12 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17beta2
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_SHA256=157af3af2cbc40364990835f518aea0711703e1c48f204b54dfd49b46cd8716c
# Tue, 02 Jul 2024 00:03:06 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:71c2dde42aad09035a9686e376c7507b6e8e2a8ada2c409775f1c1bfb8d928ea`  
		Last Modified: Thu, 20 Jun 2024 17:43:16 GMT  
		Size: 3.3 MB (3252491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a63293d280394a0a59a944bb742f8f6c68342f3e1f9bf16a6ef3ef637c089e`  
		Last Modified: Wed, 03 Jul 2024 03:34:54 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653fdd1c572b35d282f398c31bec5c106291dc280f203d420474905417452024`  
		Last Modified: Wed, 03 Jul 2024 03:34:54 GMT  
		Size: 1.1 MB (1083896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7ff659d51adccf55cc24381110b8f9b5df8525f8cd609581c42b674a625679`  
		Last Modified: Wed, 03 Jul 2024 03:34:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8aeed6c43ce929c5759d37cd07effceeb4ab24d9e1ef913901bb63bd3dc31b`  
		Last Modified: Wed, 03 Jul 2024 03:34:56 GMT  
		Size: 104.5 MB (104460473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078e14e41a48b87b5094dc59a7bd20a37bb62af0290f5f9d52dc3e83bd3e9033`  
		Last Modified: Wed, 03 Jul 2024 03:34:55 GMT  
		Size: 9.9 KB (9887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1bd3b9aa8be9df5cbecd7045d1aea7668d6905a350c5e11c60c231d695144c`  
		Last Modified: Wed, 03 Jul 2024 03:34:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96fc7e5393e82351ffb188cd32bdfc7a76da08c6eb204c51af8bf66d8b6acb01`  
		Last Modified: Wed, 03 Jul 2024 03:34:55 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb21aabe42840f016fd0679e1f5bc507090e5026b8b0eb943fa9ba2d6df7fbff`  
		Last Modified: Wed, 03 Jul 2024 03:34:56 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753ea9e1d4ac52d989e55fdfe329deee035a622b92d7e351272a18c0d3e04903`  
		Last Modified: Wed, 03 Jul 2024 03:34:56 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:18c6ec2f9c1f8cd943ff56d56850ff2515b91e8c18dd2e4c5d1a26ca145738b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **998.4 KB (998390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79057ce3b987bc78e088610418bca7c34555eb437b3d31bc847a83c8d4fd9bfb`

```dockerfile
```

-	Layers:
	-	`sha256:848f79fdbc5df9bd66c1081bdb97ad1b9f943a8b10633b76d92c861d71df3c78`  
		Last Modified: Wed, 03 Jul 2024 03:34:54 GMT  
		Size: 956.5 KB (956471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa79e787b10bad334d8f0cdc2b45a232b5db1a8fbc1c9f749be1262075c613fc`  
		Last Modified: Wed, 03 Jul 2024 03:34:54 GMT  
		Size: 41.9 KB (41919 bytes)  
		MIME: application/vnd.in-toto+json
