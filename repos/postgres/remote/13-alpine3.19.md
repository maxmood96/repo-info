## `postgres:13-alpine3.19`

```console
$ docker pull postgres@sha256:3b603b937d2e42352eeb3338143c7576003e05806a090bf6545c4ea5788687ce
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

### `postgres:13-alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:ca2348e841c18742725d61da98f259ce956929b0984ceef792e679c610398549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95891375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04d5ac7d76a7d9dc28f1cfbbef351914c92fc16a17c7a7ce5fe9bcfd881bf9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:53:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_MAJOR=13
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_VERSION=13.17
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_SHA256=022b0a6e7bc374a777eece33708895d7b60cae07d492b286b296a49d7395d78b
# Thu, 14 Nov 2024 18:53:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:53:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:53:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:53:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3801fd9ac3ee066c1de7f3d5c570d2da58ec6a0052d5a8780dc6803516e1dc6e`  
		Last Modified: Thu, 14 Nov 2024 21:10:45 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910fb82d8fc6c388a4bb0544bdef403f34d8265faf631144d8b4680e6f72b8dd`  
		Last Modified: Thu, 14 Nov 2024 21:10:45 GMT  
		Size: 1.1 MB (1120287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671036ade1d30ae3df3743f5536e8609cfe3d1e86540343d4cf85b38d0757f07`  
		Last Modified: Thu, 14 Nov 2024 21:10:45 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2733db0cef8ffb9e7753c3e964e11be3c9433be45af2e12cea56a0bcbd23bf24`  
		Last Modified: Thu, 14 Nov 2024 21:10:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43e76818df99fa7160c060c3cc905460dc530fb1d79f7558aa757ed30dcaa6a`  
		Last Modified: Thu, 14 Nov 2024 21:10:52 GMT  
		Size: 91.3 MB (91334882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363b606bf97dca7aa5490de7ded3302e652f827697de39d145168d2fd8e0f3cf`  
		Last Modified: Thu, 14 Nov 2024 21:10:45 GMT  
		Size: 9.0 KB (9016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d67d994f27cefbd647b600fa60873936a3751743633a157f42e9cb07f3f905`  
		Last Modified: Thu, 14 Nov 2024 21:10:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af081bc4f49c64c7354872206d666c8c11409cdd6d30d3ca7bd476946de328d`  
		Last Modified: Thu, 14 Nov 2024 21:10:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450c88e43ecda831f3be1da91e9e2f1a97221aed79e180ae1f9fa37ddafd0a9d`  
		Last Modified: Thu, 14 Nov 2024 21:10:46 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aaf8eec13c7f270d3c5a8dc18bb62f33a3bbe5ad92e6f2051458b5f6f86c5e2`  
		Last Modified: Thu, 14 Nov 2024 21:10:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:fb251863bba79bef2672ad538160ecf9c83b1d867dc83c263c1c552f0125c364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7912d32984854dfbeca2e206c069f7e1b1da9905c6b981c66faad85c188ea4bc`

```dockerfile
```

-	Layers:
	-	`sha256:293c26afe195e9db44961ac3751e8f6a10cb2c6cb0a151588ee6befdd6bfb024`  
		Last Modified: Thu, 14 Nov 2024 21:10:45 GMT  
		Size: 966.1 KB (966055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae8cb330bd8ad68d8b857a54cfe381b5f0de21ed396075975cea0de8423ac2b9`  
		Last Modified: Thu, 14 Nov 2024 21:10:45 GMT  
		Size: 44.7 KB (44698 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:a9ef0a77ce8f8288329815be5ce93aa63f80c3a6dfa550afcd968b881aaa4b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94360429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202b6651c269944e1584c3bc478954bf8d14b634c3679f528011f9512f7f23de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:53:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_MAJOR=13
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_VERSION=13.17
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_SHA256=022b0a6e7bc374a777eece33708895d7b60cae07d492b286b296a49d7395d78b
# Thu, 14 Nov 2024 18:53:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:53:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:53:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:53:24 GMT
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
	-	`sha256:9c7b72f7a45a2493f8b759caf574f754d907dcd8d1fd1cee201877c4ab9d2557`  
		Last Modified: Thu, 14 Nov 2024 21:44:45 GMT  
		Size: 90.1 MB (90080839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4827401dca03b83d07d55dbfd138da09889d4fc9154b6e0c1f20668051ec69e9`  
		Last Modified: Thu, 14 Nov 2024 21:44:42 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd1112c0bd73aa09393f7ef48de44e6358dbe2bfe1265eef8ab0e59768ef220`  
		Last Modified: Thu, 14 Nov 2024 21:44:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e62061277e8d4d3e96206b527952ee6a765ee98f6e5f7dc66209a3663c4b90`  
		Last Modified: Thu, 14 Nov 2024 21:44:42 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5382a3ac25791cfab3d72ecd99eddd14887e2573311fd773a30c6146a56147ec`  
		Last Modified: Thu, 14 Nov 2024 21:44:43 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062a5044be3d3f805c2123e7d8dfe2a3989f407da229464ff2d3add366503b1b`  
		Last Modified: Thu, 14 Nov 2024 21:44:43 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:0a2b94c457bb4a5c3a0c8ca025d047340f7be8b861b01f0fd89145cf229381d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 KB (44647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f179f063cc81d729a55479b6c259b0b416227edbd137a3e067ca58532e8997`

```dockerfile
```

-	Layers:
	-	`sha256:44b9cedf61225d05f1baec732612d213e469a69378dfa1fb87c1ea2e3051a102`  
		Last Modified: Thu, 14 Nov 2024 21:44:42 GMT  
		Size: 44.6 KB (44647 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:b4df9bc9dbe222813d1791c3b6e32344faf6c41b4db42d56bfe4de741a6c3578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88747427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ee2efa7d8c660e21b61075b09fb32d661603895b40e4ddb51e8ae864010d02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:53:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_MAJOR=13
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_VERSION=13.17
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_SHA256=022b0a6e7bc374a777eece33708895d7b60cae07d492b286b296a49d7395d78b
# Thu, 14 Nov 2024 18:53:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:53:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:53:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:53:24 GMT
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
	-	`sha256:9b4cc0c4a35ac123e801889db8e2a06d2f45545570454df85cae0de7fddeecc2`  
		Last Modified: Fri, 15 Nov 2024 00:13:56 GMT  
		Size: 84.7 MB (84716526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fdc549605908a4b77dca733e8e5511671dc23266adfcb8836a724ef24989a6`  
		Last Modified: Fri, 15 Nov 2024 00:13:53 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c9e1e3a77d5c4d4e27dd6bb0f425bc4878faf002627574fd0119b1d6b36f37`  
		Last Modified: Fri, 15 Nov 2024 00:13:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ca9bf8bcef3e77c1fef8f913a9d029d4db1978edc93607f80b528a9551cd7a`  
		Last Modified: Fri, 15 Nov 2024 00:13:54 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066c8fc3e6ae918e60ec7694a26616e89ab60ce3e42234b1660fc01ea5cf115a`  
		Last Modified: Fri, 15 Nov 2024 00:13:54 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de461d8f348f5d839970a693ff88dc13ebcd6fb30b67485cd0f5b907efab9a4f`  
		Last Modified: Fri, 15 Nov 2024 00:13:54 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:7790f334e366e823772fdc801ee1c3fd199df3c3095ba163a384476f4f5623d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3dec64d5940930efd06a82aa3f4b148253df33d19dbffa93f305fc3e2bb06f3`

```dockerfile
```

-	Layers:
	-	`sha256:2464e0a6a03708abfd1ad665550566fb2ed7e1a27d33b6ed5c634ecb907da9aa`  
		Last Modified: Fri, 15 Nov 2024 00:13:54 GMT  
		Size: 966.1 KB (966075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ce8bc132ee54e4f285d980da0e532c535ee16b763ee61947daa32da6252df23`  
		Last Modified: Fri, 15 Nov 2024 00:13:53 GMT  
		Size: 44.9 KB (44862 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:ab5a45321db15ac66dfba2de2626aedfd615daf628de8aeb45aef74a72144af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94528725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d58f03953096d4e5b7ef7c6f1361f52af6ce610fa1c9fc22e3a11f098d162ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:53:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_MAJOR=13
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_VERSION=13.17
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_SHA256=022b0a6e7bc374a777eece33708895d7b60cae07d492b286b296a49d7395d78b
# Thu, 14 Nov 2024 18:53:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:53:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:53:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:53:24 GMT
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
	-	`sha256:c2d7e4061b7a0932cd185c2631fb10f5a714fcca4b1fb99919faeb0f392c07c9`  
		Last Modified: Thu, 14 Nov 2024 21:46:32 GMT  
		Size: 90.1 MB (90103641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7854e11ef4e89aa766ed08a12b156316d69995025114bc87a170c4398efb2a81`  
		Last Modified: Thu, 14 Nov 2024 21:46:29 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75a7950c6c943e77c3c7092b3e3f788a675721614918894559f30aa827758cd`  
		Last Modified: Thu, 14 Nov 2024 21:46:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29a76928000018ac7d03089056e959104a027c190528c09d3500f5ee49804a1`  
		Last Modified: Thu, 14 Nov 2024 21:46:29 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19df3ac2ac4bb4f0253ee74d5e6c33303c68b4b03552e34e1cb14cbff22ea9e4`  
		Last Modified: Thu, 14 Nov 2024 21:46:30 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585239f48347c1ec93336aee025161ac02d541ac9e3d6774d26670b8f2cb46c7`  
		Last Modified: Thu, 14 Nov 2024 21:46:30 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:b8b35038f9a429ad85b26c2df9d0058cc943e1c1978d481183e22c5101a6f094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b51ca4264e45dfcb833f154f0f7e6b6205a2ea92fe95f64ed435db5b81bf53`

```dockerfile
```

-	Layers:
	-	`sha256:9ab5db9cc9e9ac15498f00d5a912e90e3c1987e9e9e42673a5a1697071845fcb`  
		Last Modified: Thu, 14 Nov 2024 21:46:29 GMT  
		Size: 966.1 KB (966087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b6ad76da9073ba1ee544aed90047ea8020960379250fa21bd223244be52d4c`  
		Last Modified: Thu, 14 Nov 2024 21:46:29 GMT  
		Size: 44.9 KB (44898 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:4ab2eb640f5a6df321daed12dae2780587b2151306b5c4c12a14372c90b0bac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100938700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3919044ad0cefc3e412032c321c70988660449e4a07b9f02cdda7d551fb3e0c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:53:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_MAJOR=13
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_VERSION=13.17
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_SHA256=022b0a6e7bc374a777eece33708895d7b60cae07d492b286b296a49d7395d78b
# Thu, 14 Nov 2024 18:53:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:53:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:53:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:53:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f2bcca8036e1665bce0b1f25104487779a51d92eb5de66915af5650de1b39e`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16545b849e3b077f6788e5894b19502c34721231b39c6960f32e6ee0f5cbbdb`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.1 MB (1095462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b409da5ad514d8a0c532e78d8b2e693b47bb93aec41476e780252d6f6b4d8a`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894b56bcddf3c86ae96ca3c02d433b5c1df7c73f50c673261c9016ab8446e7c6`  
		Last Modified: Thu, 14 Nov 2024 21:11:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9221cb5a8f294e11ed7838dbc9d2ae55a2b158252d0f824d019d7c902acf445f`  
		Last Modified: Thu, 14 Nov 2024 21:11:08 GMT  
		Size: 96.6 MB (96573099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378954aba1310b4b2a695afa22c0eab4e570d7313542bd7dc0bca9fcda89ff18`  
		Last Modified: Thu, 14 Nov 2024 21:11:05 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a81733779aa463b7fcad48323a3d1f151886b4edf005c855be1066b622524a`  
		Last Modified: Thu, 14 Nov 2024 21:11:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbec90542fbd0efdbcae2cc7186c3f379f2566b9eda4a6c126d1eb1f9165108`  
		Last Modified: Thu, 14 Nov 2024 21:11:05 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56158837b2f3076740480bcddac8356c99d22ed81edfacff6b5668d6a4eb016e`  
		Last Modified: Thu, 14 Nov 2024 21:11:06 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4ff1b2f36ace8d20aaae33c25797967839a8deb6d14f1a97b8fe53f894f675`  
		Last Modified: Thu, 14 Nov 2024 21:11:06 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:e06c6b049b9f224cc318549975b8f4f1b597c0c6e8ecc496bfc4c62d3806a178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc55e156824dbbdc9261f4b86d833626d58e0fcec0701558975f5ac404acf24`

```dockerfile
```

-	Layers:
	-	`sha256:72c0916476ac2a29cacc74462939bd542eb0262bb156ba35ccb35690b97b918e`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 966.0 KB (966040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a64fcc70218829aac8762dd9a9a4acdfa6acc874ec4512b9e9fb045c5926088`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 44.7 KB (44660 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:9bf748bb684faa966b61962bf5b5c5a970a235e88a64c3f6a36bcfe635c29c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100147020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc6bc4ff53a460690c6f940f369d6e3e7dce3c6ceaea30e303c19cf086e6c43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:53:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_MAJOR=13
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_VERSION=13.17
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_SHA256=022b0a6e7bc374a777eece33708895d7b60cae07d492b286b296a49d7395d78b
# Thu, 14 Nov 2024 18:53:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:53:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:53:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:53:24 GMT
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
	-	`sha256:927868e534e6f3a20684983094f8e1b2232ddfe8da2dcb5e559bec10b1f6be4a`  
		Last Modified: Thu, 14 Nov 2024 21:53:00 GMT  
		Size: 95.7 MB (95726342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a62b3e3ea66af0a21da3c6101737174ac3c367786ada377ecdf0fe91120214`  
		Last Modified: Thu, 14 Nov 2024 21:52:56 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab106fce3047c9b7866ca03b4d3510b2545da66c7b0914130998632628fda6e`  
		Last Modified: Thu, 14 Nov 2024 21:52:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d69a9a00263c804523d728d1e80fbd6e7226d622ef623cb93bf5910351c25b`  
		Last Modified: Thu, 14 Nov 2024 21:52:57 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae580d98a03cee59922a9744d57f504db92403c1dc9727ef561af46f6af3c6e`  
		Last Modified: Thu, 14 Nov 2024 21:52:57 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dbc1508b6a00178ecb5ca68d3df631372183cf74f28bc272f699e2d037ebc3f`  
		Last Modified: Thu, 14 Nov 2024 21:52:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:94f14ac30b0953ceaa4fe413af0bd2246c942e5600d59d4aa631e989a9ad6738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1007205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89312bfa1379d7139278d81f0181b56fba7a1950792d80137883e3bd92b72c5a`

```dockerfile
```

-	Layers:
	-	`sha256:5f2855dc9b540f5323bc016a6d6a4e854040e1056dfab07d7170a2f6580f4274`  
		Last Modified: Thu, 14 Nov 2024 21:52:57 GMT  
		Size: 962.5 KB (962459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:465bc3c4e6ee0ad22ae336fdf90cd2ec71e017fdc5b16be3ca7f79d02532004e`  
		Last Modified: Thu, 14 Nov 2024 21:52:56 GMT  
		Size: 44.7 KB (44746 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:b2f343b649865626df3544aa49213be9e3d0525a9dfb98996fd14e318dfc5985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104440070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086700c80af8c7f821e5103edf3399a5f7c2cfbdc76dbf80b7b236b620426876`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:53:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_MAJOR=13
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_VERSION=13.17
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_SHA256=022b0a6e7bc374a777eece33708895d7b60cae07d492b286b296a49d7395d78b
# Thu, 14 Nov 2024 18:53:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:53:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:53:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:53:24 GMT
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
	-	`sha256:5d41630d6a4db10719f92d059e79601e152181a27c292e9b5d2b26627f9d6e85`  
		Last Modified: Thu, 14 Nov 2024 22:26:21 GMT  
		Size: 100.1 MB (100086281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520b74564c7eaecc1ead20911ac31e4a1879933c47618aa6ab5a891376af21f5`  
		Last Modified: Thu, 14 Nov 2024 22:26:19 GMT  
		Size: 9.0 KB (9021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c595414043c6473db37bf21e14856dcd35a1227266cebe48b11572773417981`  
		Last Modified: Thu, 14 Nov 2024 22:26:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed26410e100df04a441d4fdd7ea17a085765d83be953698088008728f71ccfea`  
		Last Modified: Thu, 14 Nov 2024 22:26:19 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343cf9b7bdaf03b7a3f6fbc314142f2de58ef140ac19fc0541921e151a6aba48`  
		Last Modified: Thu, 14 Nov 2024 22:26:20 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc4912ee6e7a80519e558821cc930f4931d08232c5b29eb584a8e1b4238869d`  
		Last Modified: Thu, 14 Nov 2024 22:26:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:252de528ac19952d15bf74aa601bebe99ac7be6575088e3949b26b9af6004aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1008805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42324eeacccb4b2f0b885e94488b1c09fdf143e79a34ae721f5ac764d41294e9`

```dockerfile
```

-	Layers:
	-	`sha256:3e059f88f2141ca7c5dce487d51ba09f37e8bb49c2efa66bbe700cb669b631e8`  
		Last Modified: Thu, 14 Nov 2024 22:26:19 GMT  
		Size: 964.1 KB (964101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93a4a1b26e051fada6c07d3065e86ecc17a5aad28bd18d0073d24b28aaf0bbce`  
		Last Modified: Thu, 14 Nov 2024 22:26:19 GMT  
		Size: 44.7 KB (44704 bytes)  
		MIME: application/vnd.in-toto+json
