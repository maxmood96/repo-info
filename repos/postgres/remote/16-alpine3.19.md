## `postgres:16-alpine3.19`

```console
$ docker pull postgres@sha256:a9cb27f6696cf89cef5a2557e300964035ed661477d9497a2ce748d5da212e42
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

### `postgres:16-alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:4d3ec3d23a8f96e54154e17260e722c57c3ec9e5321f455c044a56a53b7fda92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98946502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6dbf62bbc5e63ed0daf7782acf85eb0a3bb7b938c1d82f0ac764d7315d7522`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:34:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PG_MAJOR=16
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PG_VERSION=16.5
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PG_SHA256=a6cbbb7037f98cb8afa7d3970b7c48040cf02b115e39253a0c037a8bb8e778f0
# Thu, 14 Nov 2024 19:34:05 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:34:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:34:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:34:05 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:34:05 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:34:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f83cc0245fb7bf4cda31605a8d9041f2bc49d77a07600037bc612bf6bcdb12`  
		Last Modified: Thu, 14 Nov 2024 21:10:55 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f942f143139783a3d6e91748ed5efa3c97e0f262b3ed1aa8a2e52988053b41`  
		Last Modified: Thu, 14 Nov 2024 21:10:55 GMT  
		Size: 1.1 MB (1120285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e071111baa9636124a151b495f163bbd09eadba90f58977d31878350ff5c5f`  
		Last Modified: Thu, 14 Nov 2024 21:10:55 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec540498463181fbd0790e130579bb6abc7660236e94edabfd0ad9991bb9d05`  
		Last Modified: Thu, 14 Nov 2024 21:10:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923ffd9ccc8e10e7a790a0a815479607030f088e67a1ba584c5158915d6d8b99`  
		Last Modified: Thu, 14 Nov 2024 21:10:57 GMT  
		Size: 94.4 MB (94389476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7e5911c96143feb0d5a54ee891ed791d8eedf56d67a6c403f2226fec766c7d`  
		Last Modified: Thu, 14 Nov 2024 21:10:56 GMT  
		Size: 9.6 KB (9558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149d8c7df358afde5ff53a268f2d31e0d4ec3296ce5e3da768ca18ae1049bf28`  
		Last Modified: Thu, 14 Nov 2024 21:10:56 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb337d76b3d9ad4e51e90e85b06a1a89ea52dd627827885c230030c173e393d`  
		Last Modified: Thu, 14 Nov 2024 21:10:56 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e11042de019d22315d1d0c8a86b2eb6d7afb7c0eb0b7e573e9ab4a7a7c786d`  
		Last Modified: Thu, 14 Nov 2024 21:10:57 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945af560be8607bd609debced97f25281c19b4ccb76593aa83dc8099d19e336b`  
		Last Modified: Thu, 14 Nov 2024 21:10:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:94b76bf8d1a74e057cc3d112b40b533bfe71a637ff58750d736fc6cb73b64645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c55cadc289a4e51764f6a44d7512e7b2c749f9ca8f870a9dfa125eab1a47370`

```dockerfile
```

-	Layers:
	-	`sha256:af20fa82c8b79356aa4272ae2cc11a42eb1523a03bb5c4ddb60d1cd11464e3b1`  
		Last Modified: Thu, 14 Nov 2024 21:10:55 GMT  
		Size: 969.0 KB (968999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1e1ea3917e4c46b07ebd0689623918c3310b30bbdc8318cec19350250a02420`  
		Last Modified: Thu, 14 Nov 2024 21:10:55 GMT  
		Size: 45.2 KB (45207 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:8668adb57d01fadd20bb7c9c78a3ea291a52e4665fc36f3c873770b7e0e3eb19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97326644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a7920ffab220b752fcac4718abad0ab79106c7da2f09ef14e28197acebaaf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:34:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PG_MAJOR=16
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PG_VERSION=16.5
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PG_SHA256=a6cbbb7037f98cb8afa7d3970b7c48040cf02b115e39253a0c037a8bb8e778f0
# Thu, 14 Nov 2024 19:34:05 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:34:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:34:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:34:05 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:34:05 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:34:05 GMT
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
	-	`sha256:c5f14165711f9b84e740ea9331f2b938527a0f2bc7d740761318d780d71c595a`  
		Last Modified: Thu, 14 Nov 2024 21:21:42 GMT  
		Size: 93.0 MB (93046504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42131ba8e32aa7a531cb6d56b911d33d44df720c265af7bb2baf1e73ec80f22a`  
		Last Modified: Thu, 14 Nov 2024 21:21:39 GMT  
		Size: 9.6 KB (9564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f794ddf2ffc9e07dce482d1fcb9a4e00ee2225bef0c85cb4a682b15a6f6673fd`  
		Last Modified: Thu, 14 Nov 2024 21:21:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fd43a29e9087c4d149db6ad78f64f988cb4e63648acb90e45655ee5dcc4d2d`  
		Last Modified: Thu, 14 Nov 2024 21:21:39 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6809068df774e1ed3d2d1cfe85304c9b1d089fa1edd70756a14dbf4f0ab54715`  
		Last Modified: Thu, 14 Nov 2024 21:21:40 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fbf9ac693ea1a39044533022c284f69cbdc6a97d2b33531c720b3e1aacaeb1`  
		Last Modified: Thu, 14 Nov 2024 21:21:40 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:04b3b9b87a3da205d5add62837df4fcc43c0d84c6949f92f99b7cf687b0ecbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 KB (45156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e454841fa02abf7f25559443bb4e9ec27f2651577c1c985fabae33d56e4477e`

```dockerfile
```

-	Layers:
	-	`sha256:e73880dd230f926387292ccba3dbb75faadbc5177b297e43d8572a60a450ce3b`  
		Last Modified: Thu, 14 Nov 2024 21:21:39 GMT  
		Size: 45.2 KB (45156 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:b6343398184b7c18f93c039881b6376d0b492664e002997ee5bc157c355114e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91648441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1aac256c9c82974f6bcc9942e80b742e6dc98be10960073f431c9415418a4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:34:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PG_MAJOR=16
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PG_VERSION=16.5
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PG_SHA256=a6cbbb7037f98cb8afa7d3970b7c48040cf02b115e39253a0c037a8bb8e778f0
# Thu, 14 Nov 2024 19:34:05 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:34:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:34:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:34:05 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:34:05 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:34:05 GMT
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
	-	`sha256:196fe80399117034e231f1662da4d3b758f46a36d02f713e3a662a8c6aeb6f05`  
		Last Modified: Thu, 14 Nov 2024 22:28:04 GMT  
		Size: 87.6 MB (87616992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e71ab4011aece9e6ae6ee6ad014fc37b2f06359e98c0eb516470ae1a84b1874`  
		Last Modified: Thu, 14 Nov 2024 22:28:01 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc704271cd25f7b71937afd956b7cebb6748c500aff2572d87586c5d58aaef3`  
		Last Modified: Thu, 14 Nov 2024 22:28:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a1961ba47b56dd8df83407cb22f3cf30ca77e8fb3859ecb044062295e72d80`  
		Last Modified: Thu, 14 Nov 2024 22:28:01 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a00acfd03978b73ac41e1afea69133ef5219e288b266dd995a48f571fea52f`  
		Last Modified: Thu, 14 Nov 2024 22:28:02 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e658914b724216c76e359d43f3f7e27586f42361060a1b99928ef9868401bbe3`  
		Last Modified: Thu, 14 Nov 2024 22:28:02 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:950ee24f2c1c50ec2a820aee2d4bb509fbe979477ba65b6b7361e9872ac27d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79b1109f8abc270a5539ddc76deb88ffe7ec371d4b8eb7f5ecf77dc47fb020d`

```dockerfile
```

-	Layers:
	-	`sha256:8f0fa22024a9d03f3e68783bcf45aa711289b9ed08a162cf7f1ae10eebbfffd9`  
		Last Modified: Thu, 14 Nov 2024 22:28:01 GMT  
		Size: 969.0 KB (969019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85304a3edc596cdbd7c17fe843e80dbdcd4a7aa68d689aec775fc2e134c902f5`  
		Last Modified: Thu, 14 Nov 2024 22:28:01 GMT  
		Size: 45.4 KB (45371 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:967ad88e152245c815a7302a3fea2da85276dd5b59d6ad6bae6eb2596b91f747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97545654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dabf741c843f4352760eb80be245a6c5d0b497cbf344451b8784d5310fd97263`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:34:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PG_MAJOR=16
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PG_VERSION=16.5
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PG_SHA256=a6cbbb7037f98cb8afa7d3970b7c48040cf02b115e39253a0c037a8bb8e778f0
# Thu, 14 Nov 2024 19:34:05 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:34:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:34:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:34:05 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:34:05 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:34:05 GMT
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
	-	`sha256:ee3cd88665196099595e5763f91e022dcf574dfd850d3e3653266c3539aed6fd`  
		Last Modified: Thu, 14 Nov 2024 21:22:36 GMT  
		Size: 93.1 MB (93120028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee4132f48d6803a0ab8327be5ee02a20e797a4e5d5d956771981c27730cec99`  
		Last Modified: Thu, 14 Nov 2024 21:22:33 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221a0411986e2f9a0c889ceb32ceb2daf88764444409a0e8542b7aee2f69cbd0`  
		Last Modified: Thu, 14 Nov 2024 21:22:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19602de7b1a2d53d825165e9ed55d368e5860674ac658afd7ebb7b2c958b9b93`  
		Last Modified: Thu, 14 Nov 2024 21:22:33 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32a2d21b3e570b532f858868256fd8cb533169ed5c749b2785e0af2a214b7d5`  
		Last Modified: Thu, 14 Nov 2024 21:22:34 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bc18e1ee9399e2bc97297e820b16d0a543b3830538ada4c665d9eeaf4193dc`  
		Last Modified: Thu, 14 Nov 2024 21:22:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:1342ceca3f2a61ce76435069ed28b16c8a2f107f32ef73a3127d86fc477be46b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e345e960f4df2738708bd446469e5b1cdc49059a9fbe62dab7c7c4e5bd54c8d6`

```dockerfile
```

-	Layers:
	-	`sha256:425ef9636c628f952752794f1a17e5031f16e4cbd9eb515f625158c9f144ba61`  
		Last Modified: Thu, 14 Nov 2024 21:22:33 GMT  
		Size: 969.0 KB (969031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a485a5ae3e3029a0d0ab85544743fe460a4e3decf90831c8f27f2a7fd14a61f6`  
		Last Modified: Thu, 14 Nov 2024 21:22:33 GMT  
		Size: 45.4 KB (45406 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:5f2034b987b3594bee103001aeb2b09d401701a518b7d54d77a5dd50415b8bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (104046086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733646e4e1da9c0c55d98e05745fb26c1118a21f2e14067ea9220efee644ba82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:34:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PG_MAJOR=16
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PG_VERSION=16.5
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PG_SHA256=a6cbbb7037f98cb8afa7d3970b7c48040cf02b115e39253a0c037a8bb8e778f0
# Thu, 14 Nov 2024 19:34:05 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:34:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:34:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:34:05 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:34:05 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:34:05 GMT
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
	-	`sha256:54c52297323348c66e717d25ce3263988a0a3d9fa2c605254c424c7d1a3a6aa1`  
		Last Modified: Thu, 14 Nov 2024 21:11:26 GMT  
		Size: 1.1 MB (1095474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4636e5efc47021a75b05d8197e64fa2e0af3856fd07a2aa7d7e471756bf34a39`  
		Last Modified: Thu, 14 Nov 2024 21:11:26 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9a374e9d8d67972411d17a16bdf1cf3c5acad249773bc40a018a1b312527f5`  
		Last Modified: Thu, 14 Nov 2024 21:10:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fd3beb6787f4b3bbac545df9d7d9d7ca453587a8d84eb6ff5a16d8634af3f3`  
		Last Modified: Thu, 14 Nov 2024 21:11:29 GMT  
		Size: 99.7 MB (99679926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34372c977d2636dec6d176966de33c458df527b818f93ae601182c1547ae371`  
		Last Modified: Thu, 14 Nov 2024 21:11:27 GMT  
		Size: 9.6 KB (9562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4625eb3cc01a71247633ac581ff7a6361104b78e60d0a048bd39119003d299d5`  
		Last Modified: Thu, 14 Nov 2024 21:11:27 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6e2c62d8ce408c10f68f262896988b9f82964f428c09efbd8de893b38833d8`  
		Last Modified: Thu, 14 Nov 2024 21:11:27 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f78d1c3f8f0f96a12e9edf759272dd44d5a4a4e3e1a84e9224a08f10d2e6777`  
		Last Modified: Thu, 14 Nov 2024 21:11:28 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad99a421abb640b53e333dc78d7a5cadc58a4c6b39d117b6bd94e5480e7b6d58`  
		Last Modified: Thu, 14 Nov 2024 21:11:27 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:5b1eb3d8508b6fad1456c7e692bebbccd308f79d1f04bac17502e8550cd18130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42cca6f733ca29238a3d51bb63177677c1605bc3085e46ec7c8462303ac8d504`

```dockerfile
```

-	Layers:
	-	`sha256:12a1f5a58106bcc1fb6c026f56007eb9fc1622e1c88ae2f6be5d7fd8e6e4e13b`  
		Last Modified: Thu, 14 Nov 2024 21:11:26 GMT  
		Size: 969.0 KB (968984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0779e1599b6feb392989a49eec1928f4c8b0c47fc35ffcb323fd1561675f7ad8`  
		Last Modified: Thu, 14 Nov 2024 21:11:26 GMT  
		Size: 45.2 KB (45169 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:41770d7adb6adf17203d32588eb9942fc25897044afef3e9bd3951948077d3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103383640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a4490aaaff580b3cf89a9b91c8a7f7e194d2331106d0e9da73d95572570109`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:34:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PG_MAJOR=16
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PG_VERSION=16.5
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PG_SHA256=a6cbbb7037f98cb8afa7d3970b7c48040cf02b115e39253a0c037a8bb8e778f0
# Thu, 14 Nov 2024 19:34:05 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:34:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:34:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:34:05 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:34:05 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:34:05 GMT
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
	-	`sha256:629b27832bf0828ea62bfccb4316a03312a3645c60833b592fdb648f0a63f482`  
		Last Modified: Thu, 14 Nov 2024 21:25:08 GMT  
		Size: 99.0 MB (98962410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e866dd3b97403be9540d5db280ffc13e4c335ccdfe45b52f2176f7f54ca440fb`  
		Last Modified: Thu, 14 Nov 2024 21:25:05 GMT  
		Size: 9.6 KB (9565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604bb2fd3bb08c05b87556939af1af5f1ddc07902c65f5d01e16305789f9a26a`  
		Last Modified: Thu, 14 Nov 2024 21:25:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6d962b3e35c59b7d817e1c0a9a56fbac785c0763e0c6715207c08f8738dc31`  
		Last Modified: Thu, 14 Nov 2024 21:25:05 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fbd6b8cbe78a745b4a1abb372ba1c08616f5889d58400f2086f21096b8ccf4`  
		Last Modified: Thu, 14 Nov 2024 21:25:06 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680857a300e18a2a15ef0f7eeeb9beadb91c912fde540e4abdd83503a54fe285`  
		Last Modified: Thu, 14 Nov 2024 21:25:06 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:344c510033c62a7ae86a14b839d0bf82e240beb700bc2464d891db1d4c03a56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c6e743881745c687caf985b00f3e66f5245b8fb3878e2d2fa3bc76e858c13e`

```dockerfile
```

-	Layers:
	-	`sha256:745911d9a1ea0037e225080d6f42033909fe68f1f935345e4f92bf1b74446563`  
		Last Modified: Thu, 14 Nov 2024 21:25:05 GMT  
		Size: 965.4 KB (965403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab20e1c559aaae5e5f17f36f7eb051195dd3abfbd9e65244cf598081f442765e`  
		Last Modified: Thu, 14 Nov 2024 21:25:05 GMT  
		Size: 45.3 KB (45255 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:4d8bc58af147214d3b71b5370f4742ee12dd6b963168d7168d6e6d719b5a3acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107588152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ac65af15870a83b15c4e38044a463c6140501c12e69881993faa65305915c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:34:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PG_MAJOR=16
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PG_VERSION=16.5
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PG_SHA256=a6cbbb7037f98cb8afa7d3970b7c48040cf02b115e39253a0c037a8bb8e778f0
# Thu, 14 Nov 2024 19:34:05 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:34:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:34:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:34:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:34:05 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:34:05 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:34:05 GMT
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
	-	`sha256:48124b0fd8da710382300c237733c04ed691710d08a06f2b12e7ae8e0c1970ee`  
		Last Modified: Thu, 14 Nov 2024 21:34:10 GMT  
		Size: 103.2 MB (103233811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50239a74be32c42b943b7edc40316ed67956b13ced1719242895b3e7a4f4b6a8`  
		Last Modified: Thu, 14 Nov 2024 21:34:08 GMT  
		Size: 9.6 KB (9571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da729ea3d5923585cbe043eb9656829a53ccfec122ee8d68e76436dd6d596a50`  
		Last Modified: Thu, 14 Nov 2024 21:34:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533468fca21b818e0a83080c3418504ad5f2dc14685603884a706aaca0fd56a8`  
		Last Modified: Thu, 14 Nov 2024 21:34:09 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a985ed166cd497eba79350a9064ec1758119f083aac4def7e8ed246304a392a`  
		Last Modified: Thu, 14 Nov 2024 21:34:09 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b3e49a4f08784dd47dec9b1d067567382b21adb345bd8a668c636d7249be53`  
		Last Modified: Thu, 14 Nov 2024 21:34:09 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:322f1799102518ce22fb93b1a0c0a71c2e156b75ff6dda9c629264783d2fd3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1012258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce66159a517f749c502da70b7dd1435dae957d3d3abac6cb4bab40c0f82955b7`

```dockerfile
```

-	Layers:
	-	`sha256:b2ad55a4eb616d9bbf6b3a513c6945022b04db7fb40f08e4b48233194d4375f5`  
		Last Modified: Thu, 14 Nov 2024 21:34:08 GMT  
		Size: 967.0 KB (967045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e3245090142067c718811a1e6eba8580bf8da96ba2a9a84e9675c3734954189`  
		Last Modified: Thu, 14 Nov 2024 21:34:08 GMT  
		Size: 45.2 KB (45213 bytes)  
		MIME: application/vnd.in-toto+json
