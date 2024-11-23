## `postgres:14-alpine3.19`

```console
$ docker pull postgres@sha256:d27f13914958b522ecb0838221cbadcb53f22eec45b443ffbfd1aa807684dbd1
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

### `postgres:14-alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:4e26af2cab57ab0ac9262a23bd8a3b6729c5d23f03cf2289250cb90a9e7d9cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97405720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7effec2e0eb7e8df305f664071826d0a0d114394e94b252ccf0b6e8d825d5dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_MAJOR=14
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_VERSION=14.15
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_SHA256=02e891e314b4e9ee24cbd78028dab7c73f9c1ba3e30835bcbef71fe220401fc5
# Thu, 21 Nov 2024 20:09:59 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:09:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:09:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:09:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bf21ab08380cb19e9624c7cef9be79dee0d32c6ac2ce33f8bda0ffae4660fe`  
		Last Modified: Fri, 22 Nov 2024 20:27:41 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05ff72e9f8fe7d6493096a512b5f4a093ef190100135bcd2efdc2e5b39584b5`  
		Last Modified: Fri, 22 Nov 2024 20:27:41 GMT  
		Size: 1.1 MB (1120289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523c281912c03f700879af140b801b6346052da1953801dbb6affc402338dee8`  
		Last Modified: Fri, 22 Nov 2024 20:27:41 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095410c00d8c662d31134a2c6bc6eefeef1af745df97c8e23bbe7c9030e9653b`  
		Last Modified: Fri, 22 Nov 2024 20:27:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcadbfcb8d64d09f54688c77537ac29be847985f91926f06679d2d76d3bbe87`  
		Last Modified: Fri, 22 Nov 2024 20:27:43 GMT  
		Size: 92.8 MB (92849051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64142802fb8f3411505a2f21d011443eee7131bc37f4ac7d06717790b1d1bd2`  
		Last Modified: Fri, 22 Nov 2024 20:27:42 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443fb87c2cca7ac7ff83951a5939a59c4d1b0225c6121056c5e79544f2347559`  
		Last Modified: Fri, 22 Nov 2024 20:27:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c63c4224c87fe7949ccac9247242d9125d41a0a2fdcc1d45725d969866e0e95`  
		Last Modified: Fri, 22 Nov 2024 20:27:42 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c487aaae42c59cd4ee16800a67c8d99a418174ec2ef85d87821b57ed2b770c`  
		Last Modified: Fri, 22 Nov 2024 20:27:43 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7658b706ba4df59348ad4329d8e4353dbc4b36b7fc47806495b1364e276717`  
		Last Modified: Fri, 22 Nov 2024 20:27:43 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:df20c1e0e8a18d4630370bd6441042f3a9a154127ed04b526bba135f3f7347bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1013982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583c6e63b273aaecc4edfc8939152cf3a1ea54e91c8893ef2d22e2f7ecd47ada`

```dockerfile
```

-	Layers:
	-	`sha256:aed56856ae4c3358b21667edd3827577829234cb7c13e8fe3203e6358be706fc`  
		Last Modified: Fri, 22 Nov 2024 20:27:41 GMT  
		Size: 969.0 KB (969003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc62f1132a29b0c4d63fe138accf6c09c83c496e550ccbb5722375aefc4886a9`  
		Last Modified: Fri, 22 Nov 2024 20:27:41 GMT  
		Size: 45.0 KB (44979 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:6a66ea5bd33e882388b5d756435d128505299dd4710630171f59607ff339d1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95844524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b029933b3ab4e026d3d2e850943aae6d8c68aa070c34e390ce3d63d4fde1a324`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_MAJOR=14
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_VERSION=14.15
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_SHA256=02e891e314b4e9ee24cbd78028dab7c73f9c1ba3e30835bcbef71fe220401fc5
# Thu, 21 Nov 2024 20:09:59 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:09:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:09:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:09:59 GMT
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
	-	`sha256:e48112f21acc3d46e1be3653e67f7eabb485cd400560e864a25826702da5cd34`  
		Last Modified: Fri, 22 Nov 2024 20:55:33 GMT  
		Size: 91.6 MB (91564750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286d7db7c401c65e98263d72f0c0374b0d9448dcfe94fbeb5b1987e8e9e11148`  
		Last Modified: Fri, 22 Nov 2024 20:55:31 GMT  
		Size: 9.2 KB (9202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875b7cf4de04743544df66424ada4e13835d575345e0da672f02deb03c9b65a7`  
		Last Modified: Fri, 22 Nov 2024 20:55:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b71697554251261bdbbc3e0e04f371464538d44a6ed6bac2610898a52e68a1`  
		Last Modified: Fri, 22 Nov 2024 20:55:31 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9da4f718cc106891558939721f23cf5987c92daf38af0efa50996c317e64a4`  
		Last Modified: Fri, 22 Nov 2024 20:55:31 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aa814d2c18767ae05b8ce568480acabaa0afd0f84793aede530a48bb1fa1ed`  
		Last Modified: Fri, 22 Nov 2024 20:55:31 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:07320477be7d8c29eec2c07eb16e2f237cb6ae674c1abf2e04de378ef8d944d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 KB (44928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ef04773adf3ab7837a0a2f640f3e8f7a9d6d0add4601840f6d43ead96f7257`

```dockerfile
```

-	Layers:
	-	`sha256:f5ca87bb1df442b74099922600bb223fe38a6ea5cd08f548e1e795ccf337c45a`  
		Last Modified: Fri, 22 Nov 2024 20:55:30 GMT  
		Size: 44.9 KB (44928 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:e2fcb9b4647a83462ec9e18f27557ffa588bde75e002990250ce71dd88671725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90187701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a75eb130be0c5ce7940baa96d75feee6e2b0ee8eb7234e3c6570916a9c22a1ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_MAJOR=14
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_VERSION=14.15
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_SHA256=02e891e314b4e9ee24cbd78028dab7c73f9c1ba3e30835bcbef71fe220401fc5
# Thu, 21 Nov 2024 20:09:59 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:09:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:09:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:09:59 GMT
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
	-	`sha256:2fa1eb3cdbe7dd9dd8446491ea2eb0cae164014c578420a2caf474fe738eb031`  
		Last Modified: Fri, 22 Nov 2024 22:54:25 GMT  
		Size: 86.2 MB (86156607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5aea3cccb48c5a48abed000f2f641710e6c47484610fe10697cc3709bb7574d`  
		Last Modified: Fri, 22 Nov 2024 22:54:23 GMT  
		Size: 9.2 KB (9206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85827e6837cf53cf5484508d0941c78ca3f4793bbd03558ba60de47babcedefe`  
		Last Modified: Fri, 22 Nov 2024 22:54:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8aa0149fec7f2457b9abd1f58b62c01ddaffcdf46cd37361abbdcb91be8da4`  
		Last Modified: Fri, 22 Nov 2024 22:54:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2bec9ecc7efd10118a6f13892776f05609e05344e44ef2d97d2325fe580592`  
		Last Modified: Fri, 22 Nov 2024 22:54:23 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11aa61c3552773a9bbc4dc21d654c8be6bd73689c32a4dcaee5628c40cde4488`  
		Last Modified: Fri, 22 Nov 2024 22:54:24 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:05c483967db93ab4f7485b520d0fb5ca143e6a6005837c4ca0fcd759c3cb8fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca975c36dc84ec85ba57c2c3714c2d484de0d3e733c51ea7f300e23146221e81`

```dockerfile
```

-	Layers:
	-	`sha256:a11d0317a6f577d90dcd752360528118d4d9f52efbe151b33b18e8a94d110857`  
		Last Modified: Fri, 22 Nov 2024 22:54:23 GMT  
		Size: 969.0 KB (969023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3534bf790e0f531725a71edf8358ee237b80dd7978e521b4b480ed82256c0c7`  
		Last Modified: Fri, 22 Nov 2024 22:54:22 GMT  
		Size: 45.1 KB (45142 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:a6393843d60b7169c72624b76ec046e706d748fc813e9f03dd87b69fc120c2f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96010938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55667ce4a1f83983e36307ec142eba6078e26da9d97a9fc2b012cc3b0ca3f7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_MAJOR=14
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_VERSION=14.15
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_SHA256=02e891e314b4e9ee24cbd78028dab7c73f9c1ba3e30835bcbef71fe220401fc5
# Thu, 21 Nov 2024 20:09:59 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:09:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:09:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:09:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12908080ef4c1fe1084233332d7f38ee24d4d9205cf67d2efaaf56b48161c8`  
		Last Modified: Fri, 22 Nov 2024 20:34:07 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108f2378d159809cd20c16968f33184d490c2aeb6efac4b1ab24cb3014f9012e`  
		Last Modified: Fri, 22 Nov 2024 20:34:07 GMT  
		Size: 1.0 MB (1049362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56e305cc8981dd87964d1f003a738a758f1d1875083f70573b5ec28ec25e1a1`  
		Last Modified: Fri, 22 Nov 2024 20:42:10 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66eff82c1eeaedb859d806f658b6b1559962da775f8f66e9a8de0a5763a5868f`  
		Last Modified: Fri, 22 Nov 2024 20:42:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5a83fbd9ede0cbd5a8305dcde98feffede96a29eb942ca455861fab90fc1b3`  
		Last Modified: Fri, 22 Nov 2024 20:57:53 GMT  
		Size: 91.6 MB (91585668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9cd75f2a480bb6bd7faefcbf33626987846dc051bdda53e93ca5679b3d520e`  
		Last Modified: Fri, 22 Nov 2024 20:57:50 GMT  
		Size: 9.2 KB (9202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5550446844c0fcf09c852411b3ec1883ddc55b0b1888e83b73125f42088179d`  
		Last Modified: Fri, 22 Nov 2024 20:57:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460e17ef4f272a43a83ef9d05dce41d34931da499a3bf6cc9ffe7b7978ef034c`  
		Last Modified: Fri, 22 Nov 2024 20:57:50 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b2e4e4bef84ac00e9a8bbe34734f96091ab0ee7568e23181bb1ad1f7dde9a7`  
		Last Modified: Fri, 22 Nov 2024 20:57:51 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a47792eabc2b3c92cb899fd2711eb36f717f1401ddf664438a722fe37f9d554`  
		Last Modified: Fri, 22 Nov 2024 20:57:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:7677fc7fcde00ff298fb657c7fe7ce9cb4c877493a349956a47bf542f80ea476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1e59dc0826092a47d98b4deddb7abde2c15d67ab9741ffb0569f5ce70a3951`

```dockerfile
```

-	Layers:
	-	`sha256:f3f03b17b718152b4f03230a77d63e1e7a3253ea4c1c2265ce9b0b5649015a21`  
		Last Modified: Fri, 22 Nov 2024 20:57:50 GMT  
		Size: 969.0 KB (969035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a08aad28735b43c70a229fd14fb563d41b8aeec5a7c5811aff92a686625e6e5`  
		Last Modified: Fri, 22 Nov 2024 20:57:50 GMT  
		Size: 45.2 KB (45179 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:fc5141ff127b20123d1c4ec6ae80fcb91df06a6550268693fababf9e9f5a0ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102503546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574b59073d087d2db74231c392678e9b242191e3b6f037d95e63870b1a5cf015`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_MAJOR=14
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_VERSION=14.15
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_SHA256=02e891e314b4e9ee24cbd78028dab7c73f9c1ba3e30835bcbef71fe220401fc5
# Thu, 21 Nov 2024 20:09:59 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:09:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:09:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:09:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69283567ee862552e281a4ca04e68ba279bb36d4f2e4d9a07b35c9d9b8788e8`  
		Last Modified: Fri, 22 Nov 2024 20:28:13 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a868a02b0bd97e4ac3196ad2ec5de798fc18d79914239c00f3dff3758882cb`  
		Last Modified: Fri, 22 Nov 2024 20:28:13 GMT  
		Size: 1.1 MB (1095467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db83ad258737fc893a7505d695e9e53f8e723952d87593398d4a42309903e78`  
		Last Modified: Fri, 22 Nov 2024 20:28:13 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da39b9160ac48afed55f58463a46b2ef1d6355c04c66cd272b8a6818c9ac54f6`  
		Last Modified: Fri, 22 Nov 2024 20:28:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8ce42b0c5dcb308ac18bf07b20ff48eb97563bdb68c256ff3ff14d06da689c`  
		Last Modified: Fri, 22 Nov 2024 20:28:16 GMT  
		Size: 98.1 MB (98137760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db8ccbaa61a8aae80e0e8e727372abc06d3614471fe93440d1d4b902269ac1d`  
		Last Modified: Fri, 22 Nov 2024 20:28:14 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c62eb4026ead1489c5743437a42913d2f13b890701829f8861a497867b7155`  
		Last Modified: Fri, 22 Nov 2024 20:28:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0846c89e122f2329fd1d6bdcbebfac84e3ceb9beb85c6cccdced91b7cb4f93a5`  
		Last Modified: Fri, 22 Nov 2024 20:28:14 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e8057ca47bc7067f9dfe50e383b51a64a66419e95e029c03af61b1a991c470`  
		Last Modified: Fri, 22 Nov 2024 20:28:15 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64afb3ff7eacfa03a9578bb38628fe3f2d5af71c3188ca753bfc2d0f95edec30`  
		Last Modified: Fri, 22 Nov 2024 20:28:15 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:f653a72c9e1c6d300b796c437f767d562515f0924e0105b0a464572420729cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1013929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe63e5800105cb98aac7c6f4d263c5d4a95a1d7d2e446bb92b48635b55b65c28`

```dockerfile
```

-	Layers:
	-	`sha256:1f36d4f2774a4e4c4184896353a93673ae61c389153781cbadb0d1a65d9a5c17`  
		Last Modified: Fri, 22 Nov 2024 20:28:13 GMT  
		Size: 969.0 KB (968988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85ff68293ffedbe156fadd76181cc0bc60bc447eff3fe256733c794a13646d77`  
		Last Modified: Fri, 22 Nov 2024 20:28:13 GMT  
		Size: 44.9 KB (44941 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:55e4eec0ac359094307d63880e6e744f0ad75aa554dbf5688e8e318ae4e82718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101764594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a14a4bb9e71b6deb85d50e2a58bfca6521223d49a3bbcfbe08500ed65f405b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_MAJOR=14
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_VERSION=14.15
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_SHA256=02e891e314b4e9ee24cbd78028dab7c73f9c1ba3e30835bcbef71fe220401fc5
# Thu, 21 Nov 2024 20:09:59 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:09:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:09:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:09:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b210ec8ed1260138487b366b6cc6cf870563d4506a35f0a64ccdc7db288b503`  
		Last Modified: Fri, 22 Nov 2024 20:39:39 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f569b818764a75b625723057d18967c65a9adae20004f6d1aa2a6a6f141f80`  
		Last Modified: Fri, 22 Nov 2024 20:39:39 GMT  
		Size: 1.0 MB (1039701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63aaaafb14cd321df8b5ca67c848dc45a2338f4035ab70e99b0ac6389005a932`  
		Last Modified: Fri, 22 Nov 2024 20:49:33 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f154c1764c5654b15d98e0100301c9ff6316930d0b36d0661aae65faff846b4c`  
		Last Modified: Fri, 22 Nov 2024 20:49:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d32d58755ccc0e3aaf0a795b0f6a0db02a0831eefc7d480398ba0309044b7e`  
		Last Modified: Fri, 22 Nov 2024 21:08:32 GMT  
		Size: 97.3 MB (97343720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0774804e5df64e45d7338fe86854ae5922ccba046b585c48a7c52f826eecaf1`  
		Last Modified: Fri, 22 Nov 2024 21:08:28 GMT  
		Size: 9.2 KB (9206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ede8d29b3bc8a8f88160a24f3d5d67efcd0a7656c09daa8773ce9f401fc34cc`  
		Last Modified: Fri, 22 Nov 2024 21:08:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839dc9ffc5e590556c2659eac938e52014a2d68ee9ce999cbe53e228cfdb216c`  
		Last Modified: Fri, 22 Nov 2024 21:08:29 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e16eff31f3ffb759bf7c88107c1bbfd63528e5a76b7c097e8f462afba8d806e`  
		Last Modified: Fri, 22 Nov 2024 21:08:29 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273480a5799eab4807923f303abeebdd66e24c060393a6f39c566d4059aa56ce`  
		Last Modified: Fri, 22 Nov 2024 21:08:29 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:e06a0da20355f2c0b4f7d7b333add7ac96025df4b0c8c286b1da7c319420169f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e94825791e74c9834a0dc6c9b800b0f022fcb57a6a5195c8ed56d1eca716578`

```dockerfile
```

-	Layers:
	-	`sha256:07868f11ceb0839992bb1af6e851dfdf7dcddbad49b5229751c3254c19aa5fc6`  
		Last Modified: Fri, 22 Nov 2024 21:08:29 GMT  
		Size: 965.4 KB (965407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f295dbeb548d6197a74d647fae3c2b034d18ebf54eebb5afa7e45a57c9e3a29`  
		Last Modified: Fri, 22 Nov 2024 21:08:28 GMT  
		Size: 45.0 KB (45027 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:c8cc53cac240336b4cefdd51f65e519f72589848e8b215eecbc01565aab04323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (106031515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bc82c98d8293be591e508b2426cfc3c199a3b0f4de18e76364e18ff6baf101`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_MAJOR=14
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_VERSION=14.15
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_SHA256=02e891e314b4e9ee24cbd78028dab7c73f9c1ba3e30835bcbef71fe220401fc5
# Thu, 21 Nov 2024 20:09:59 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:09:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:09:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:09:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7508d4d6ac64ab81f5f150e33662bfd19f23a5c43a2e417c08da4ef9669ea599`  
		Last Modified: Fri, 22 Nov 2024 20:36:47 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50692ebd9455b35336c3bbf6d65952fc740571194ad1404bee4b68c65a2d5eda`  
		Last Modified: Fri, 22 Nov 2024 20:36:47 GMT  
		Size: 1.1 MB (1083900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0fc7b1619a2ef674c606069a975f0de7c57938bd6bd30094ae92a0850cb056`  
		Last Modified: Fri, 22 Nov 2024 20:46:08 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec9e98c8f2fafd55b33b7ef1022974a43f4a5dcfd94b9c1258dbaf476372cb6`  
		Last Modified: Fri, 22 Nov 2024 20:46:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3385ce7f2cff69f14ad49bde6ab7a574c0e011cfe7a54c2f1b433bc5a7a7d2dd`  
		Last Modified: Fri, 22 Nov 2024 21:07:20 GMT  
		Size: 101.7 MB (101677555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fad8d8a687e3adf3300bcc615dfdd2fa86408922f1d5877f5849f4306ceccee`  
		Last Modified: Fri, 22 Nov 2024 21:07:18 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10e009e89f8668ebc8db9276d87d6c92302d5e8aa1d1bfd95c0f6770f35f213`  
		Last Modified: Fri, 22 Nov 2024 21:07:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe6023ca2b29c21b1a4f9a379bf7bfbc79e2b4d0395731eb3fbc6807e80b837`  
		Last Modified: Fri, 22 Nov 2024 21:07:18 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76914348b1e78638ebc7fbb7227cd26ec5bb935a040d11798baea65676658a4`  
		Last Modified: Fri, 22 Nov 2024 21:07:19 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bb31d6f8c4ee18f1a77ac6b791c67834ed333fb0f85d2291b570044e5b2bbb`  
		Last Modified: Fri, 22 Nov 2024 21:07:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:c91559af1a64e3894a90768ed63c361b8473a5cd345ba5be8cb286c4b5420be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1012034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b45128f8669be980d7dadb261f648c32efd518c0e9ec4726be4ab5fa3549c9`

```dockerfile
```

-	Layers:
	-	`sha256:7c6167147c22d067da79a75e46ce8035f3a77b7b60ba571feee2ca7d3c7d375a`  
		Last Modified: Fri, 22 Nov 2024 21:07:18 GMT  
		Size: 967.0 KB (967049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b88f2bfc4faf1a174c92e1137007b6d841ab81bd2310e3a519ec8a00dccf002c`  
		Last Modified: Fri, 22 Nov 2024 21:07:18 GMT  
		Size: 45.0 KB (44985 bytes)  
		MIME: application/vnd.in-toto+json
