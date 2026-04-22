## `postgres:14-alpine`

```console
$ docker pull postgres@sha256:d796d1043e40be9a83a08cb95532154391cf3198767efe232293a7b39d45440d
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

### `postgres:14-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:8b3b0d3f7ba1468a84a64b27a012fcdaf55aa54155ee9598f60218e3bfee0998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108548980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ba25d000cf8898b7ab1181101ff191dc459ed1100020c724980697d8e802df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:09:33 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 21 Apr 2026 23:09:36 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:09:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:09:36 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 21 Apr 2026 23:09:36 GMT
ENV LANG=en_US.utf8
# Tue, 21 Apr 2026 23:09:36 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Apr 2026 23:09:36 GMT
ENV PG_MAJOR=14
# Tue, 21 Apr 2026 23:09:36 GMT
ENV PG_VERSION=14.22
# Tue, 21 Apr 2026 23:09:36 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Tue, 21 Apr 2026 23:09:36 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:11:49 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:11:49 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:11:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:11:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Apr 2026 23:11:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 21 Apr 2026 23:11:49 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 21 Apr 2026 23:11:49 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:11:49 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:11:49 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:11:49 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:11:49 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc6c8191e953b1c252ac626cc3d1303ad1175a561ac50eac72bd5f32d2f92a9`  
		Last Modified: Tue, 21 Apr 2026 23:12:05 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e565ede0467b7987401791f14144d09001523acbf44ce0025964fe3975190e7`  
		Last Modified: Tue, 21 Apr 2026 23:12:06 GMT  
		Size: 919.1 KB (919056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca57b1559f58e1848986a5d94481f4ed6392fd17b61dcaa5c344a94043896980`  
		Last Modified: Tue, 21 Apr 2026 23:12:05 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e7803864adafe3c13e27bf1243cdc6e6270f5ecb889337b2288cad96facbbb`  
		Last Modified: Tue, 21 Apr 2026 23:11:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f5cbd161cc086bbb33f89b2a9922e4b229ac2a42542d06241c20441a400b4f`  
		Last Modified: Tue, 21 Apr 2026 23:12:08 GMT  
		Size: 103.7 MB (103748693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8494b0f851610f347b05522ba50feaa64e216ea782dc36037392739c5b1414c0`  
		Last Modified: Tue, 21 Apr 2026 23:12:07 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbd169469e9188a4f384ede34753ca685142a8472600f3fc17d87f180821e9f`  
		Last Modified: Tue, 21 Apr 2026 23:12:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62258b0e2d88b38f803ed586639c136398ff12c2443d4aa2434fdb489340c2de`  
		Last Modified: Tue, 21 Apr 2026 23:12:07 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd3a9ae51e8cc8ffa92c2b210b6ff8826380838c2b86360a217082fe2c0446c`  
		Last Modified: Tue, 21 Apr 2026 23:12:08 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dddf68975e828d4b108588942822fc6160e2303f7cf4d012d51d864ceeb7a42`  
		Last Modified: Tue, 21 Apr 2026 23:12:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:0b529b314c7ce2a8a6afbfb563c1a64ee5b2ed2b12f90a6228d6b40745647a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.2 KB (642179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7329c170ae26b9c3792eed7d8bf66d9b35708a3b1dd17d0eac57468cc6b9ecca`

```dockerfile
```

-	Layers:
	-	`sha256:e55ea6fc1362037904d351d981fa8a6c985d77c8e1757bd8b5f0396260ba77fb`  
		Last Modified: Tue, 21 Apr 2026 23:12:05 GMT  
		Size: 598.1 KB (598108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:880cb495e65ce4df83a00e1936edab4be8f859eaf20d00cd7e4e88049be32f4a`  
		Last Modified: Tue, 21 Apr 2026 23:12:05 GMT  
		Size: 44.1 KB (44071 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:5e44da450687fddd0e11f6720e9c9b6fc9cd0961f860e8f2f0d4cc8dbd16e380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88051914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816db1444c05a0d8aa03592b6c63e887ae95fe371c91336a17140b60031431bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:20:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 21 Apr 2026 23:20:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:20:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:20:19 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 21 Apr 2026 23:20:19 GMT
ENV LANG=en_US.utf8
# Tue, 21 Apr 2026 23:20:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Apr 2026 23:20:20 GMT
ENV PG_MAJOR=14
# Tue, 21 Apr 2026 23:20:20 GMT
ENV PG_VERSION=14.22
# Tue, 21 Apr 2026 23:20:20 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Tue, 21 Apr 2026 23:20:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:23:02 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:23:02 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:23:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:23:02 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Apr 2026 23:23:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 21 Apr 2026 23:23:02 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 21 Apr 2026 23:23:02 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:23:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:23:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:23:03 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:23:03 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:23:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368e3c17dc958537a8127fc590105c82e6acb4ca0fa08421da0e983915a73cbc`  
		Last Modified: Tue, 21 Apr 2026 23:23:13 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3657cb2ce3fe127db8e85e0bfcb29227fbfd383ad1e3578e4b2f036705efcdd5`  
		Last Modified: Tue, 21 Apr 2026 23:23:13 GMT  
		Size: 887.1 KB (887117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f3936cf19109356d09dd190159944ac979dcb314b42f9445661686a3dcd4b7`  
		Last Modified: Tue, 21 Apr 2026 23:23:13 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc48fbb6e1adc94e64925a69cf7dd533dcde37e70546072f47f77f81d0b164d`  
		Last Modified: Tue, 21 Apr 2026 23:23:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02672af21a8781a60deab9e30a2bc7d928a2f585d499c70d962473ad66da4217`  
		Last Modified: Tue, 21 Apr 2026 23:23:16 GMT  
		Size: 83.6 MB (83575894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d21c432c0ab022021610ca2aea1ab8ecd8cf09a7f0bf3524094c0bfdafca29f`  
		Last Modified: Tue, 21 Apr 2026 23:23:14 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3751a2c350885ec18342dc9c5fad54053a7156bf0ea35e9b42eb0e1885cbc533`  
		Last Modified: Tue, 21 Apr 2026 23:23:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe5d5a6538fcc95ce4378d1421c17ebd133cfb1b647b5cbf1a908d71f777d6b`  
		Last Modified: Tue, 21 Apr 2026 23:23:15 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05304f10bdea7b37f4854731e28f1e7b624b1df1855bf1b9bc10f0c23d5e50f`  
		Last Modified: Tue, 21 Apr 2026 23:23:16 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384aad5f0428002c2f3be01cab330aeae3f9525156f62c1ff2a91d3949082fd4`  
		Last Modified: Tue, 21 Apr 2026 23:23:15 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:1c7d881135a944e7b16bcef3f6c4401c685216eb35b4e67da5007cd252e26727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 KB (44034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62817cd1eb68f3f145d7ba28b9503b6a41eee5f99554e5fd2c55fabb4360238`

```dockerfile
```

-	Layers:
	-	`sha256:fe7fa3585a5a5a9ac8ba0daa50e88ba14853ce6c9e9850f3fb7fb6ff1452294e`  
		Last Modified: Tue, 21 Apr 2026 23:23:13 GMT  
		Size: 44.0 KB (44034 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:613f21ea974278eea2eaa43ce81031ae749c7d32170465aa8a16f25f6b110aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83323839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1349ce8fe6f9ea3344d0dc9bd9098f49f6d27dfae0217c268751ba7c83ebc62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:36:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 21 Apr 2026 23:36:18 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:36:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:36:18 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 21 Apr 2026 23:36:18 GMT
ENV LANG=en_US.utf8
# Tue, 21 Apr 2026 23:36:18 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Apr 2026 23:36:18 GMT
ENV PG_MAJOR=14
# Tue, 21 Apr 2026 23:36:18 GMT
ENV PG_VERSION=14.22
# Tue, 21 Apr 2026 23:36:18 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Tue, 21 Apr 2026 23:36:18 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:42:02 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:42:02 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:42:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:42:02 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Apr 2026 23:42:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 21 Apr 2026 23:42:02 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 21 Apr 2026 23:42:02 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:42:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:42:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:42:02 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:42:02 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:42:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856f214be977f8b813c31348e4a3c1b73eddb595b6aa632b428650f020ad0964`  
		Last Modified: Tue, 21 Apr 2026 23:39:13 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9be6c27fcd6ad5c9a9dd4ad4b9955009b2e44e003936a2a42cefbf24ed8bba4`  
		Last Modified: Tue, 21 Apr 2026 23:39:13 GMT  
		Size: 887.1 KB (887123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0317de0846692d8fa8a9b5de95643ddbcfc365e10002f741a757c99456401c`  
		Last Modified: Tue, 21 Apr 2026 23:39:13 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa642d7b40b4257f14a4c05d61f008b0545c3ca2977ab91965cd3d31f8dd5af`  
		Last Modified: Tue, 21 Apr 2026 23:39:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b527ecc8ecd310da2c9ff4c9f516024c1cd6d06d066226c836d1c6c3cab075c1`  
		Last Modified: Tue, 21 Apr 2026 23:42:16 GMT  
		Size: 79.1 MB (79136553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6e25e8dac9d64312fe10c20eb3a24e05292184f7e8e1b3d5f2dc6a88d8868c`  
		Last Modified: Tue, 21 Apr 2026 23:42:13 GMT  
		Size: 9.2 KB (9206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156b9d969e2597d82560cc1c4aa93dc95447a2623038eb0fc0bc041472f34ad7`  
		Last Modified: Tue, 21 Apr 2026 23:42:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150a4d64631e3d3d14478f8a18768fddcc6a0351684e411eeb7f360725f5efad`  
		Last Modified: Tue, 21 Apr 2026 23:42:13 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f597ccc898a2b2e2273611e9c666e99becc32b4d43a36dcc54d44cf31ddc52`  
		Last Modified: Tue, 21 Apr 2026 23:42:14 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1c03774942096f4d11dcc23488ef19f5e21df0f8e3ff3571e9661e637014b8`  
		Last Modified: Tue, 21 Apr 2026 23:42:14 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:0278d826030475a850c9b2dda0523643094513a292cc33d8e65686731bd63dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.7 KB (641743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc4b1b854d49367df04926666990552659453a0fac859779061f911436e84bd`

```dockerfile
```

-	Layers:
	-	`sha256:ca9ed3256728d6f1f6f59cd728fd7b2f6031d74d7efd18095648cf84675f89fe`  
		Last Modified: Tue, 21 Apr 2026 23:42:13 GMT  
		Size: 597.5 KB (597494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70ff34ac719461c2268740c0dc481cadcaff2da05cd7741b59ab2d4ee60044ff`  
		Last Modified: Tue, 21 Apr 2026 23:42:13 GMT  
		Size: 44.2 KB (44249 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:52cbc16140128880f23b833533c3d54a3adca0d2ff6454c6456f3d7c7f75f230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106760969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3754534f0f10346037fe3119f9ce505192a950e80fc77b6b3ce70457316f52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:08:03 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 21 Apr 2026 23:08:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:08:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:10:54 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 21 Apr 2026 23:10:54 GMT
ENV LANG=en_US.utf8
# Tue, 21 Apr 2026 23:10:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Apr 2026 23:10:54 GMT
ENV PG_MAJOR=14
# Tue, 21 Apr 2026 23:10:54 GMT
ENV PG_VERSION=14.22
# Tue, 21 Apr 2026 23:10:54 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Tue, 21 Apr 2026 23:10:54 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:13:01 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:13:01 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:13:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:13:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Apr 2026 23:13:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 21 Apr 2026 23:13:01 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 21 Apr 2026 23:13:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:13:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:13:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:13:01 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:13:01 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:13:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1340dca956dcd0427021db688d1bcbdcf4fcb541e64f48ba28383f1ba04b83bc`  
		Last Modified: Tue, 21 Apr 2026 23:10:46 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207c1ffa3c37802f66a02ec01c37f0b06d291d081a25ff5bc0a7a9467ebc8682`  
		Last Modified: Tue, 21 Apr 2026 23:10:46 GMT  
		Size: 874.7 KB (874711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561e1742aa9408534f3220cb8b7960e3d8147cb8c77b31bd14cbd6553525c2e1`  
		Last Modified: Tue, 21 Apr 2026 23:13:16 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486cbdfe5bda8f8e5cc2fba056530a60d9f7bc2524e866d9490da3498080905d`  
		Last Modified: Tue, 21 Apr 2026 23:13:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b395ab304738a54ed6bd80192e9ea6921c8bf78ca7b87981cd01aa77bade3f9`  
		Last Modified: Tue, 21 Apr 2026 23:13:19 GMT  
		Size: 101.7 MB (101669348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd4b11bb97e43290cc3fa7d4e0a9ed80b66e2bd0f34cb229a00364bc2715050`  
		Last Modified: Tue, 21 Apr 2026 23:13:16 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0882085722eab1717dadd660c1fd06e588ccf9e5475e0cef66397c936d60507`  
		Last Modified: Tue, 21 Apr 2026 23:13:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa1c862d9f026c8e88b3469f6fe238abdb308395dee2f99af9b1811bbe5c50a`  
		Last Modified: Tue, 21 Apr 2026 23:13:17 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb6dbd4225696e704491821e7fd2da968fbdb071732c1496eb9a62d3479c0ab`  
		Last Modified: Tue, 21 Apr 2026 23:13:18 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f27458befa6e2bc7e0c4471db3057196856ee6a6d52b842b6dc8025a4d62035`  
		Last Modified: Tue, 21 Apr 2026 23:13:19 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:47af00ef92014b67a2405a539fe2d242e4f7f1ba6a424ecaf5eb1fcc4b4c26fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.8 KB (641808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54984b5bc0aba38555289aba3ea4ad65504733cd3b7e174b6e854bcb830abd3c`

```dockerfile
```

-	Layers:
	-	`sha256:991e58f54cb9145e305aeed8e9adae82a6b8f40c6be8c285b028bc05cd14ee7f`  
		Last Modified: Tue, 21 Apr 2026 23:13:16 GMT  
		Size: 597.5 KB (597514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190ae5bcb87ae8ffd00c44a40a6a984b3b1690633b0bcb887e2a5182e3c51871`  
		Last Modified: Tue, 21 Apr 2026 23:13:16 GMT  
		Size: 44.3 KB (44294 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine` - linux; 386

```console
$ docker pull postgres@sha256:f1209e6457bd3d87bb64f84b4649571dddd75cda3ae0717da5db7901ce675344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114578253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9637079bca3175a262f0b6597eab3b5b0deba8df703ab47253eb447d831d297`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:15:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 21 Apr 2026 23:15:18 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:15:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:15:18 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 21 Apr 2026 23:15:18 GMT
ENV LANG=en_US.utf8
# Tue, 21 Apr 2026 23:15:18 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Apr 2026 23:15:18 GMT
ENV PG_MAJOR=14
# Tue, 21 Apr 2026 23:15:18 GMT
ENV PG_VERSION=14.22
# Tue, 21 Apr 2026 23:15:18 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Tue, 21 Apr 2026 23:15:18 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:20:29 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:20:29 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:20:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:20:29 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Apr 2026 23:20:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 21 Apr 2026 23:20:29 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 21 Apr 2026 23:20:29 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:20:29 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:20:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:20:29 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:20:29 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:20:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9725ff196d61a24c41d17f58262fb93e9f991fb0f743a7e0691f14c044a56e6`  
		Last Modified: Tue, 21 Apr 2026 23:17:58 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed279c6555471a55a488619b4be60bf8d6b8d5ff752488f624aed3d495256806`  
		Last Modified: Tue, 21 Apr 2026 23:17:58 GMT  
		Size: 891.6 KB (891645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0a98a2482673f22caafd03247c2ddbe99885d0b0473de9fcb30797a2fd1c9`  
		Last Modified: Tue, 21 Apr 2026 23:17:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59052b9efe2504b4dfa38b7a47d64fafac779ca15c83faf29b6dcbb87c4f183`  
		Last Modified: Tue, 21 Apr 2026 23:17:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc03fc9edfd85467da98650697748a8c14c1ab177d58bb983aace2d92f650400`  
		Last Modified: Tue, 21 Apr 2026 23:20:49 GMT  
		Size: 110.0 MB (109979118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee402d8912f25d5761e1000464f92a8d2523b3a60454fc7d84e8ce0802807989`  
		Last Modified: Tue, 21 Apr 2026 23:20:45 GMT  
		Size: 9.2 KB (9206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5fa7888a27ff9966839c7d7b78c1e1ec8bd9efdd7bec2553830366be14d387`  
		Last Modified: Tue, 21 Apr 2026 23:20:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd90d217bd749aa97177a2c60a73f5a24be8a30f32a3b8d4302a60e5f700d159`  
		Last Modified: Tue, 21 Apr 2026 23:20:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfd59bdcdfc32af76ca144c368b9df7289de4fe4ccb41de89dcf5dc386fea23`  
		Last Modified: Tue, 21 Apr 2026 23:20:47 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb93144f72fa13cb04abdf6512c171dda0dc44267ee499d3173bc89990d2b502`  
		Last Modified: Tue, 21 Apr 2026 23:20:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:d368ebd2e942a9059920607d84ee48caab77cfbe29077d0c1001a371f9d80761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.1 KB (642106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbed66bbb980d05247c52b6352e6a08c096d6246f9a142e880438dda21b2b10`

```dockerfile
```

-	Layers:
	-	`sha256:251dcb0f270a82b5041c46a1b428da86b3640f1f8a29f1751b1160263e63db9c`  
		Last Modified: Tue, 21 Apr 2026 23:20:45 GMT  
		Size: 598.1 KB (598083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25ba5cdf228d29508764c98dcab7cf1a5af01dc3894d76fb91d02805fbb985c8`  
		Last Modified: Tue, 21 Apr 2026 23:20:45 GMT  
		Size: 44.0 KB (44023 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:f50a22d3a34b70c2b82dd62d9cc8a83da84fbc6c0f82faa218e0f8f64c2faccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93399319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9363d95e8639a5a0ca691d6792d7463cda0013bffdfd73cb292ed010c0948703`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:55:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Apr 2026 20:55:24 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 20:55:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 21:00:23 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 15 Apr 2026 21:00:23 GMT
ENV LANG=en_US.utf8
# Wed, 15 Apr 2026 21:00:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 21:00:23 GMT
ENV PG_MAJOR=14
# Wed, 15 Apr 2026 21:00:23 GMT
ENV PG_VERSION=14.22
# Wed, 15 Apr 2026 21:00:23 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Wed, 15 Apr 2026 21:00:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 15 Apr 2026 21:08:10 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 15 Apr 2026 21:08:11 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Apr 2026 21:08:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Apr 2026 21:08:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Apr 2026 21:08:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Apr 2026 21:08:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 21 Apr 2026 23:52:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:52:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:52:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:52:46 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:52:46 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:52:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9504179c89581170cbe497b214c2f97f01eae1cac5905e1d1fafdcf5bc01926d`  
		Last Modified: Wed, 15 Apr 2026 20:59:59 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a284924cfe2e8e2e82ff8309f349edbdfa04cfaa5de86e49b14e6cb75225a`  
		Last Modified: Wed, 15 Apr 2026 20:59:59 GMT  
		Size: 880.1 KB (880126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdbf69e74f8065c17f9aae6946c699680b19b0f5dac3b0eb9d86c6b4d150805`  
		Last Modified: Wed, 15 Apr 2026 21:04:25 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40505d0bc2ac480cc189bc63f3786b58510be6cd3ab7577555a65b6258920690`  
		Last Modified: Wed, 15 Apr 2026 21:04:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb42def7c828a2cefaa1de4239c824caa4cbfaedee8db85ae09ceb51c18cb47`  
		Last Modified: Wed, 15 Apr 2026 21:08:42 GMT  
		Size: 88.7 MB (88671214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6a8bbb75091c641b5448172848c0eefed944fde161969b39b89400b58407a5`  
		Last Modified: Wed, 15 Apr 2026 21:08:39 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8910090a6b676250442d4b436b08eb8119c19740d38c54bce38caa1f9525fc`  
		Last Modified: Wed, 15 Apr 2026 21:08:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e80a3a4503f76c9d9d7627c63bc6fea004d22911f49fdcc95c1d772cab5a287`  
		Last Modified: Wed, 15 Apr 2026 21:08:39 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ab370a03c9a2e514f60465a452411d76586d218904c2d18a4df7de9a58c117`  
		Last Modified: Tue, 21 Apr 2026 23:53:06 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef319f0c26b36503f0cef2f7b2ae95596c4aec7439ce91b3b322351025146478`  
		Last Modified: Tue, 21 Apr 2026 23:53:06 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:703e7eef26bdd9ba9de368d6251e05e71064a0227b173ab30cd22d7e7e8628fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 KB (639954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd212e5f92a08c5ab6aa448d607943a231463886993bac98c4ad25b3bd6ef06`

```dockerfile
```

-	Layers:
	-	`sha256:abbbb78c7d83c364ec207278acd3663b0c6200c2b32ffeb15e2ff55572fdb13c`  
		Last Modified: Tue, 21 Apr 2026 23:53:06 GMT  
		Size: 595.8 KB (595829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceb99a0f538a93bae6a7a52e97414ea14cbfb78b175e08b762f81f6ba37b3710`  
		Last Modified: Tue, 21 Apr 2026 23:53:06 GMT  
		Size: 44.1 KB (44125 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:1bac27b6f332592de3bc854d48e4b4a5245c17a8f0cc8ce4eb7e35ec81ab6675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109464480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9796df80fba567691b50d3b4b3b0b0cb88069af8f8b8dfe621d08ed16a7d58ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 11:29:33 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 16 Apr 2026 11:29:45 GMT
ENV GOSU_VERSION=1.19
# Thu, 16 Apr 2026 11:29:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 16 Apr 2026 13:20:58 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 16 Apr 2026 13:20:58 GMT
ENV LANG=en_US.utf8
# Thu, 16 Apr 2026 13:20:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Apr 2026 13:20:59 GMT
ENV PG_MAJOR=14
# Thu, 16 Apr 2026 13:20:59 GMT
ENV PG_VERSION=14.22
# Thu, 16 Apr 2026 13:20:59 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Thu, 16 Apr 2026 13:20:59 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 16 Apr 2026 15:54:45 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 16 Apr 2026 15:54:45 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 16 Apr 2026 15:54:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 16 Apr 2026 15:54:45 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 16 Apr 2026 15:54:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 16 Apr 2026 15:54:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 16 Apr 2026 15:54:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 15:54:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 16 Apr 2026 15:54:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 15:54:46 GMT
STOPSIGNAL SIGINT
# Thu, 16 Apr 2026 15:54:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 16 Apr 2026 15:54:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c05352c3bc3bad2a071af544c560bfc66f25f632b9841754ed94c4abb19732`  
		Last Modified: Thu, 16 Apr 2026 12:22:58 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0841d6e8e03b3f5779ff0c2893e4e26e90895e6f4a7ec62726ad628be33e10e`  
		Last Modified: Thu, 16 Apr 2026 12:22:58 GMT  
		Size: 867.5 KB (867538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01640490039f18e0efc72dfc7e79e994ee5239169b238b30d21ba147a4d3d087`  
		Last Modified: Thu, 16 Apr 2026 14:14:12 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba82bcb214ae71de3d2b623be98402bc90b03aef6f555c7dd3f2d1a2a3676e2`  
		Last Modified: Thu, 16 Apr 2026 14:14:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c2852132fd7b92d77ae4256a477d20e2fbb5b61873942a1f4f26bc72648e5e`  
		Last Modified: Thu, 16 Apr 2026 15:57:47 GMT  
		Size: 105.0 MB (104992477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbb6ce77886aeba2f943d19bf4a454b1a7180f6aa59e83e0cba142ae8ef39e7`  
		Last Modified: Thu, 16 Apr 2026 15:57:32 GMT  
		Size: 9.2 KB (9214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72721799be3010480ed4883cfe0c55e92b6162805472fa68f602e3b4ea01dda`  
		Last Modified: Thu, 16 Apr 2026 15:57:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92935cab6e9cb32fb76c3195bf016c163d48291fb7ef86ec2c3402b1524ee90d`  
		Last Modified: Thu, 16 Apr 2026 15:57:32 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fc696b565a96bbcf6c0eea948c85dfcfa56d64e6c9e51ab29d2eedf060de43`  
		Last Modified: Thu, 16 Apr 2026 15:57:33 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9da275a96fd0caed57cb2959e94510166db8e7f59fa407d73c4d94cc5acb10d`  
		Last Modified: Thu, 16 Apr 2026 15:57:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:0c48728ac8c3e7df2e6a7136faeee6f3f539862976d0b1d3d10dea29a8476e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 KB (641618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f90a443bd6f62dc5343ec1feb5033f4b6f94648d0cc09c1db07fc6495d3759`

```dockerfile
```

-	Layers:
	-	`sha256:e232e15129a6e5a24b91b7a4d9bf391a23b40a999251994752c2c45ee5143d9f`  
		Last Modified: Thu, 16 Apr 2026 15:57:31 GMT  
		Size: 597.5 KB (597487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174184a13585852798aa5f1377e073b142ee939c39b20631b95e3b86242d22cc`  
		Last Modified: Thu, 16 Apr 2026 15:57:31 GMT  
		Size: 44.1 KB (44131 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:75714b5c0f273960f76b2c8034f0e90c4fbadafd6ac0796a0167e5f9be678cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116677853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2c38f1738370b9dc7613cc1c93af145e413aac49078d69372313ae7f0155cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:32:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Apr 2026 20:32:28 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 20:32:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 20:37:51 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 15 Apr 2026 20:37:51 GMT
ENV LANG=en_US.utf8
# Wed, 15 Apr 2026 20:37:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:37:51 GMT
ENV PG_MAJOR=14
# Wed, 15 Apr 2026 20:37:51 GMT
ENV PG_VERSION=14.22
# Wed, 15 Apr 2026 20:37:51 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Wed, 15 Apr 2026 20:37:51 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 15 Apr 2026 20:41:50 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 15 Apr 2026 20:41:50 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Apr 2026 20:41:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Apr 2026 20:41:50 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Apr 2026 20:41:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Apr 2026 20:41:51 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 21 Apr 2026 23:42:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:42:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:42:46 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:42:46 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:42:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c5ed854292088ad91fb5a623e51a3682312408cead42a22166de3fd8d1dc8a`  
		Last Modified: Wed, 15 Apr 2026 20:37:29 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ce62b957b857c08f679922ba4b91dc49057c951937637dd94b40a7fe8c5b81`  
		Last Modified: Wed, 15 Apr 2026 20:37:29 GMT  
		Size: 895.8 KB (895798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae20370d30162e578ddc4261332750d5420660a4b540ba6effcd03e08803223b`  
		Last Modified: Wed, 15 Apr 2026 20:42:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2957e716cf88c06abe669da7b50ef11d5b4dd8a2518ba299f5cc206a57082586`  
		Last Modified: Wed, 15 Apr 2026 20:42:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d314077ae85e6aaca9d7d27874337835053d80d57b6453153e4b049861043eb3`  
		Last Modified: Wed, 15 Apr 2026 20:42:18 GMT  
		Size: 112.0 MB (112038469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4ca017b083e36c20f2e1a80e8f37258d1ee0a55b5da0a6472d63662f73888d`  
		Last Modified: Wed, 15 Apr 2026 20:42:16 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5339a768d607e062c915dd3cb6a06d45742b8e2ca79b8d195202e970fc421030`  
		Last Modified: Wed, 15 Apr 2026 20:42:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c467eb9303242e61b0e1938c50bfb9386f2a83c879db3ccccb3ee53b5e38a3`  
		Last Modified: Wed, 15 Apr 2026 20:42:17 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bedcffd47f511542eb96c6716047042d4b52d026b2b93e02e7c88e5628860c`  
		Last Modified: Tue, 21 Apr 2026 23:43:00 GMT  
		Size: 6.1 KB (6104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506b4dcdfc5cc63f4df28e694bc18cc41a5ccf03f06b035bcff2124436b50ef4`  
		Last Modified: Tue, 21 Apr 2026 23:43:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:ff9da332f7422b244f75a999bf2c221096fa4f726202ae63c987bfb2b552b77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.5 KB (641528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a810ff4c972cc2d04fda055b1ee5693535fc2ca37c78953223f38be81124eeb`

```dockerfile
```

-	Layers:
	-	`sha256:8eecd557ecd8a44c38ce5cce096047972b5f13f1b68ead9aa8f97d35ae8ea24b`  
		Last Modified: Tue, 21 Apr 2026 23:43:00 GMT  
		Size: 597.5 KB (597457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beb9475beb0298434e4f8eb6ecf3be3df977cb80e419e59ef7f7ba6fd7aaedac`  
		Last Modified: Tue, 21 Apr 2026 23:43:00 GMT  
		Size: 44.1 KB (44071 bytes)  
		MIME: application/vnd.in-toto+json
