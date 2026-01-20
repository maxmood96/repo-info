## `postgres:18-alpine3.23`

```console
$ docker pull postgres@sha256:b40d931bd0e7ce6eecc59a5a6ac3b3c04a01e559750e73e7086b6dbd7f8bf545
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

### `postgres:18-alpine3.23` - linux; amd64

```console
$ docker pull postgres@sha256:6723ec6d445fe51c6d097b9248f8a4b793255853524839fca1b2d69a435b6072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.0 MB (111951386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9a5682d571fa93a90e4fabd8821c43d887b70fbe7b2f4a80bb57799ed6350e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:36:49 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 00:36:52 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 00:36:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 00:36:52 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 00:36:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 00:36:52 GMT
ENV PG_MAJOR=18
# Thu, 18 Dec 2025 00:36:52 GMT
ENV PG_VERSION=18.1
# Thu, 18 Dec 2025 00:36:52 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 18 Dec 2025 00:36:52 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 00:39:07 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 00:39:07 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 00:39:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 00:39:07 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 18 Dec 2025 00:39:07 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 18 Dec 2025 00:39:07 GMT
VOLUME [/var/lib/postgresql]
# Thu, 18 Dec 2025 00:39:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:39:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 00:39:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:39:07 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 00:39:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 00:39:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a9324a2bdc71b64dbb5798a8b73ac1ab91dff051e2c54e6ceda752210b1a22`  
		Last Modified: Thu, 18 Dec 2025 00:39:33 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e827ac0fa1ea70150fe4cbbf6939c188e6a44c97f19ab2c56e89191ad73df01`  
		Last Modified: Thu, 18 Dec 2025 00:39:33 GMT  
		Size: 922.9 KB (922945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0629ac8b8cc524f650b1ee707708ca100b2d66bf4fc5784063db1fe02efe4826`  
		Last Modified: Thu, 18 Dec 2025 00:39:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e50a444bddfdbf4681296a3391bc525c280f5df4e8df98e75ff5f943cace5d2`  
		Last Modified: Thu, 18 Dec 2025 00:39:48 GMT  
		Size: 107.1 MB (107142140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4465107e1675e81b1843ac03422aebe8f8a211f4b68500cdb3335698104046e3`  
		Last Modified: Thu, 18 Dec 2025 00:39:33 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2ee20b6816a3adf820d9dd82172e42a12791b7524c5d64ab107bfbe5f733a0`  
		Last Modified: Thu, 18 Dec 2025 00:39:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfd86289dd1ce111fd67dc1625a1a53c3a97c9109877e142f924b77caf4fbf7`  
		Last Modified: Thu, 18 Dec 2025 00:39:33 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98eecc0da868b41cc3f8b99805d29675ea70e0a8680eaeb60670bffffe3f74f1`  
		Last Modified: Thu, 18 Dec 2025 00:39:33 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b747867e61cbade8fac8813031bdcb3e09756b92a9116c5b29017ca390024207`  
		Last Modified: Thu, 18 Dec 2025 00:39:26 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:929c69807ea91db30046f05054db18bfd9270b80da01cd380e61f5f5a7af48a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.4 KB (643423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6aa42265c99e9aa7a70459e54f5750b1e1d33feb1c7d5a37244bc73dbef12a4`

```dockerfile
```

-	Layers:
	-	`sha256:38d11430027420634077461d7f69af959b4bd985f5848e5901fb61edc664bbc6`  
		Last Modified: Thu, 18 Dec 2025 03:11:32 GMT  
		Size: 600.3 KB (600312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cc9201299e50eb2f1a2e5d1dcdd560227f093daaaa28dbeaa34b73b0e659438`  
		Last Modified: Thu, 18 Dec 2025 00:39:23 GMT  
		Size: 43.1 KB (43111 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.23` - linux; arm variant v6

```console
$ docker pull postgres@sha256:70be7607da70693096a6f80f2a8a657ee3699aaf4c793c5d1248899441e9deea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91421424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa8d76c86a3578e00d2982da0b176a64e67ee1e0ddeca361e401d68a282cc746`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:44:42 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 00:44:46 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 00:44:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 00:44:46 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 00:44:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 00:44:46 GMT
ENV PG_MAJOR=18
# Thu, 18 Dec 2025 00:44:46 GMT
ENV PG_VERSION=18.1
# Thu, 18 Dec 2025 00:44:46 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 18 Dec 2025 00:44:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 00:47:36 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 00:47:36 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 00:47:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 00:47:36 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 18 Dec 2025 00:47:36 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 18 Dec 2025 00:47:36 GMT
VOLUME [/var/lib/postgresql]
# Thu, 18 Dec 2025 00:47:36 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:47:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 00:47:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:47:36 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 00:47:36 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 00:47:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb1338ad38fbe457cff0eef9964a724acbbfdd43caabfee8cf29eb3459e7998`  
		Last Modified: Thu, 18 Dec 2025 00:47:47 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b194cda91b6a94af3348c878e9f25b3303e5f2af8d17d7111e4ed1346610e0`  
		Last Modified: Thu, 18 Dec 2025 00:47:54 GMT  
		Size: 889.5 KB (889470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd29e571df216763b8a9a7b405cea0b6ef7cc3071aa22381872451f65380ae5`  
		Last Modified: Thu, 18 Dec 2025 00:47:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a222b473aaae4595e3d4638d698c0cf904872d3928f381bf9f1e90db0b89b127`  
		Last Modified: Thu, 18 Dec 2025 00:48:02 GMT  
		Size: 86.9 MB (86937332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe68d020bfe136bbfa8c6c07fa218cfe743dabbc2771e4a52a7c9eb9945b876`  
		Last Modified: Thu, 18 Dec 2025 00:47:48 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496e35e55459e3559d9927de770dfacd1004876415a20ab8ca6a9541af86767a`  
		Last Modified: Thu, 18 Dec 2025 00:47:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da3f4ef29cac882b9b908db8d69438188cdc2a84fb668a3aebb89d844484e5a`  
		Last Modified: Thu, 18 Dec 2025 00:47:49 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8bc6043a09873ea8818706b03ce04b9c30bfcc062a7d9fd0670046602f0b0b`  
		Last Modified: Thu, 18 Dec 2025 00:47:54 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e1633f37e841b99445bad01eb59578e2c5a665a7e75d20762ee13e8b6bb2b8`  
		Last Modified: Thu, 18 Dec 2025 00:47:50 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:052fffe21ebece353fd7f6db27acb0947a3a96eba0d45b78d636da61c5098087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 KB (43076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185af0be490abb544c28d1a97b9e63e9ca10b577aa969233d774b7696326928f`

```dockerfile
```

-	Layers:
	-	`sha256:852e5f454cd513db1dcad574a7ddb86b11bb982184270410b8074b8ad9d9a8bf`  
		Last Modified: Thu, 18 Dec 2025 03:11:37 GMT  
		Size: 43.1 KB (43076 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.23` - linux; arm variant v7

```console
$ docker pull postgres@sha256:5bef6a648062aa61118a62d864c18298e5281fb23405989818fdd2e13cc712a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86571573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e21c29f4addd0bd61200c2d759d8fe3a66236314a33b3b0d762343aa13d9a15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:45:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 00:45:27 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 00:45:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 00:45:27 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 00:45:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 00:45:27 GMT
ENV PG_MAJOR=18
# Thu, 18 Dec 2025 00:45:27 GMT
ENV PG_VERSION=18.1
# Thu, 18 Dec 2025 00:45:27 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 18 Dec 2025 00:45:27 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 00:48:10 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 00:48:10 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 00:48:10 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 00:48:10 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 18 Dec 2025 00:48:10 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 18 Dec 2025 00:48:10 GMT
VOLUME [/var/lib/postgresql]
# Thu, 18 Dec 2025 00:48:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:48:10 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 00:48:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:48:10 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 00:48:10 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 00:48:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57c54560c889f4335681276f8006934bf52e4b177d237ff206c5dd5983c093f`  
		Last Modified: Thu, 18 Dec 2025 00:48:29 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9357d8fc3629d45c7e5e204823a20084bc2d55d8be9f123aacbde58e2854e15e`  
		Last Modified: Thu, 18 Dec 2025 00:48:29 GMT  
		Size: 889.5 KB (889513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c7a206a04af5b574ce4649140e77522ce3aafe0d14371cc15ccd1062b47f86`  
		Last Modified: Thu, 18 Dec 2025 00:48:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfcf7ab8b514d4cf91ab2018f45636d0b889076ba436b8bcb0878cabfe4437c1`  
		Last Modified: Thu, 18 Dec 2025 00:48:39 GMT  
		Size: 82.4 MB (82376477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13958f2c6b0a555a1bcfc8e628bd5c91202d609aa6e44fb564108cea93054ac`  
		Last Modified: Thu, 18 Dec 2025 00:48:23 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb52157d722bfd08a0f1c188758cbe032a4e8f8885f52f9883c537e2e1f0236`  
		Last Modified: Thu, 18 Dec 2025 00:48:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a81e22e662dd6d0d7d0e3bd15fc5fbeb5b188979af7458f70af2547d27e311`  
		Last Modified: Thu, 18 Dec 2025 00:48:29 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1867e68f5d02198ed68b0683922ae793010b29b9f92bcdd9294d443633b0959`  
		Last Modified: Thu, 18 Dec 2025 00:48:29 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ff24c1e791225620bc70c341190b350885f1cace069c4ba21c22c4ebdc96e0`  
		Last Modified: Thu, 18 Dec 2025 00:48:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:cb290cbf14515af47064e24f8dc15154cd8e33a5d8ea061de9e6db6fde1c5ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.0 KB (643007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1faa9b74c5ee42172352d884e951930200139adc9ad42112e384dad02ab1aad`

```dockerfile
```

-	Layers:
	-	`sha256:4e0fa26b13d4e508c1fd798f828b82c6628302270c97b456b3063c8c30ec4bca`  
		Last Modified: Thu, 18 Dec 2025 03:11:40 GMT  
		Size: 599.7 KB (599714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aef6b5e5beeec6e875a0fb452afcbbb3028a9d2fce72032811870af8e2d47d01`  
		Last Modified: Thu, 18 Dec 2025 03:11:41 GMT  
		Size: 43.3 KB (43293 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:289cd9c63ca1a9c4c2e9c301211448dfccdbd0eef6ff1f7d01e451705ed8d32b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110131944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71da06f54e40c03d845d6ca5bdd23ced5ac0beb63fc2fad2e7a072a8fa86b24e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:36:01 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 00:36:04 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 00:36:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 00:36:04 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 00:36:04 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 00:36:04 GMT
ENV PG_MAJOR=18
# Thu, 18 Dec 2025 00:36:04 GMT
ENV PG_VERSION=18.1
# Thu, 18 Dec 2025 00:36:04 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 18 Dec 2025 00:36:04 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 00:38:31 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 00:38:31 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 00:38:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 00:38:32 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 18 Dec 2025 00:38:32 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 18 Dec 2025 00:38:32 GMT
VOLUME [/var/lib/postgresql]
# Thu, 18 Dec 2025 00:38:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:38:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 00:38:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:38:32 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 00:38:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 00:38:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e78006cc964e3458d4451d94fedb9f6083bb8a0c8c5b15195170dcef0afe871`  
		Last Modified: Thu, 18 Dec 2025 00:38:53 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4978a67dfd653a5ddac678360cb0c9d5a3991cd8e033a2bd826af3725406234`  
		Last Modified: Thu, 18 Dec 2025 00:38:53 GMT  
		Size: 876.5 KB (876476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab151012693c0fb503e33db0c80dacec3b11d295a6107bcc29057cabcf7983f1`  
		Last Modified: Thu, 18 Dec 2025 00:38:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4a5c5df1ab62f115c20de68ec795ee7d1e07fa12403e4a94b0c4eeef5f3d03`  
		Last Modified: Thu, 18 Dec 2025 00:39:10 GMT  
		Size: 105.0 MB (105033537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8196dfb248d2eae0fa9f783c04506456e5066c097a51e61f730d08258445a747`  
		Last Modified: Thu, 18 Dec 2025 00:38:53 GMT  
		Size: 18.8 KB (18775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d714fe9da766b086fdd45d7da56ca5a35632213cc08cb4c07797f4323d3e1c10`  
		Last Modified: Thu, 18 Dec 2025 00:38:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fedec264dfecef24f7ede36bd4432c2fa37e0e022832b71cd7237b34d92bf3bf`  
		Last Modified: Thu, 18 Dec 2025 00:38:53 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9912675a8fda3806c230b8069bbca214945d56edda947eac3db4447703203c5f`  
		Last Modified: Thu, 18 Dec 2025 00:38:49 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c220efb4f6bbb60fea5912555cee3d4a954b926728681c00d4a910135025db96`  
		Last Modified: Thu, 18 Dec 2025 00:38:49 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:99db58976a6ac02de80e10ff8e5534f1337f4f1bfc38354507a302928d642a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.1 KB (643087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e02582a10c4417b444ee0e1467ca0a308f7e0fbc6b66fe44f32400b96db9251`

```dockerfile
```

-	Layers:
	-	`sha256:af6e95b6a8c00a8418a77bd8de1e109305803af8eedbd7ae841b4b236b27579c`  
		Last Modified: Thu, 18 Dec 2025 03:11:44 GMT  
		Size: 599.7 KB (599742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:273511c1d62d44919ad0c6f4f66b25320884ba2a71523c9ec615e5d4ca0f1bd5`  
		Last Modified: Thu, 18 Dec 2025 00:38:47 GMT  
		Size: 43.3 KB (43345 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.23` - linux; 386

```console
$ docker pull postgres@sha256:754cb2deb52294a7c5d7fa0560f0bb036e27f674934d33803c763e078233b35e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118113785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee276fbce9803dbdb16bfd572786ef035fa1058763a26710839642136d5ec361`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:37:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 00:37:59 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 00:37:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 00:37:59 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 00:37:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 00:37:59 GMT
ENV PG_MAJOR=18
# Thu, 18 Dec 2025 00:37:59 GMT
ENV PG_VERSION=18.1
# Thu, 18 Dec 2025 00:37:59 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 18 Dec 2025 00:37:59 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 00:40:31 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 00:40:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 00:40:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 00:40:32 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 18 Dec 2025 00:40:32 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 18 Dec 2025 00:40:32 GMT
VOLUME [/var/lib/postgresql]
# Thu, 18 Dec 2025 00:40:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:40:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 00:40:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:40:32 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 00:40:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 00:40:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0b79147c2775f71b3a9344cb66a6ce09eccec5aa1afd2eaa1a3b2496fea16a`  
		Last Modified: Thu, 18 Dec 2025 00:40:48 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc31caab6b7379f4126860c1278c8c142671fd1678f43ed9d73381159a9e2a2d`  
		Last Modified: Thu, 18 Dec 2025 00:40:56 GMT  
		Size: 893.2 KB (893244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8865fe3b5e3bcd086dc5abcb0ba0bbfacc783ac27c6b542a39752132d873f6a9`  
		Last Modified: Thu, 18 Dec 2025 00:40:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded0a07b980e53e0a915d962486a055c5ec4bb83467754d7b240112f39baccfd`  
		Last Modified: Thu, 18 Dec 2025 00:40:51 GMT  
		Size: 113.5 MB (113508239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a460de82bb5c6134e0f2420dbc946e633a9e4ec6b85032bda3638f8d19ca5e6e`  
		Last Modified: Thu, 18 Dec 2025 00:41:00 GMT  
		Size: 18.8 KB (18775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7839484665f2d36d3202b0c9117a899bfbbe0d8697d9ac75e865f90c4060be60`  
		Last Modified: Thu, 18 Dec 2025 00:40:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e76d8040c663733be1ffbf983578edcd100c59e3c525d93d84d794074e0d63`  
		Last Modified: Thu, 18 Dec 2025 00:40:49 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75935a808894da128a656b7d319fa047afdf774b8b0f7a9758178d4d39ef18ce`  
		Last Modified: Thu, 18 Dec 2025 00:40:50 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19db13356dec485fc7a4141f05c2515c3bd3ee17c21e91479733cd9bd77a778a`  
		Last Modified: Thu, 18 Dec 2025 00:40:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:2951689fdee2125d11d906be481310140a5a763dbd675c1c0d6d08f15615c265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.3 KB (643333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba41f98e1a0566d373cd6c31fed1bac80623d06902d1be3a6c9118ea05dd1f3`

```dockerfile
```

-	Layers:
	-	`sha256:a23e57c362852d9f37ca876a13ba982c4881664265baa5895e5f755ed77e5fd0`  
		Last Modified: Thu, 18 Dec 2025 03:11:49 GMT  
		Size: 600.3 KB (600277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11c9a4f2ecd5346ff413cbd9d955b369ad9b406f17deaac611d32e0b5118094f`  
		Last Modified: Thu, 18 Dec 2025 03:11:50 GMT  
		Size: 43.1 KB (43056 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.23` - linux; ppc64le

```console
$ docker pull postgres@sha256:f0ef0a54edcaf62933223db28a2c6bfc0c32da9714e92446aefac217fdaed96e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97051269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b67b4c2887169ada17bb5fbe9b28a4a63b4ac6f5a6bd10190cc0ab905540485`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:23:31 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 01:23:37 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 01:23:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 01:23:37 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 01:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 01:23:38 GMT
ENV PG_MAJOR=18
# Thu, 18 Dec 2025 01:23:38 GMT
ENV PG_VERSION=18.1
# Thu, 18 Dec 2025 01:23:38 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 18 Dec 2025 01:23:38 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 01:26:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 01:26:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 01:26:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 01:26:16 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 18 Dec 2025 01:26:17 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 18 Dec 2025 01:26:17 GMT
VOLUME [/var/lib/postgresql]
# Thu, 18 Dec 2025 01:26:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:26:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 01:26:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 01:26:18 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 01:26:18 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 01:26:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff80bfb816c7f5a841f48ccc8340de9f38d3ad53202d1114a5d309378c7e4c`  
		Last Modified: Thu, 18 Dec 2025 01:26:51 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a7bf1ce9f177344350a6b5de388d3492ef2eee83822d55eb5653a1e893a773`  
		Last Modified: Thu, 18 Dec 2025 01:27:00 GMT  
		Size: 881.5 KB (881524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545f07d641b6033697f25c011ee3e2bf820df61d9fd27c6c458f4c42259e6829`  
		Last Modified: Thu, 18 Dec 2025 01:27:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580d140e416943955f305cb58c4f08ffc298a8c6d24c0cf98a56a974c833db4d`  
		Last Modified: Thu, 18 Dec 2025 01:27:11 GMT  
		Size: 92.3 MB (92315784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4364287a9b7d5124040460d44089ff451071b22623a65ea5a864064c0ffa37d`  
		Last Modified: Thu, 18 Dec 2025 01:26:52 GMT  
		Size: 18.8 KB (18785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996da3054bf89df583d06a35581b6264f525ab1ab4a2fc8b9a0d9b2fc347621d`  
		Last Modified: Thu, 18 Dec 2025 01:26:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d1405981c9d413fcb97f0eab599f2418925077c32bea77a06cfac9f94f0cb7`  
		Last Modified: Thu, 18 Dec 2025 01:26:53 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea67119c58d2ef3abb24c2d3c8986213d92f6ce4cf5fe7d14169db1f0d928a51`  
		Last Modified: Thu, 18 Dec 2025 01:27:00 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951c4f32ea08ef87669c7a546c8ed36221ac99ac539de80cd16047924a06b166`  
		Last Modified: Thu, 18 Dec 2025 01:27:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:cc3e04f75fbd03d0b13ea9ceb20e4f342092d483171c4348ead5b0dcdba85ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.2 KB (641221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7f3159b569e4ae068ecfc76ec6562be09069b0548915e6519852c48ce71280`

```dockerfile
```

-	Layers:
	-	`sha256:2eafdd55bbc11fe093daa974763601780683d8d5b50bb186cab64de781b988d7`  
		Last Modified: Thu, 18 Dec 2025 03:11:55 GMT  
		Size: 598.0 KB (598045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:810a0f3d0e8b4c58adc3dee4a05f95e7c1c3894acf6115b75e6c434819764983`  
		Last Modified: Thu, 18 Dec 2025 03:11:56 GMT  
		Size: 43.2 KB (43176 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.23` - linux; riscv64

```console
$ docker pull postgres@sha256:0bdf47bd7a6be5c2805df68ca0489d9c9cfeee1b7bc228b977109b16b4d8bfaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113209112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650b60de93541fc796472df7ed3059e337252ea5de860e5848d0c8d15ec5e4d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 22:58:49 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 22:59:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 22:59:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 22:59:01 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 22:59:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 22:59:01 GMT
ENV PG_MAJOR=18
# Thu, 18 Dec 2025 22:59:01 GMT
ENV PG_VERSION=18.1
# Thu, 18 Dec 2025 22:59:01 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 18 Dec 2025 22:59:01 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 23:49:10 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 23:49:11 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 23:49:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 23:49:11 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 18 Dec 2025 23:49:12 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 18 Dec 2025 23:49:12 GMT
VOLUME [/var/lib/postgresql]
# Thu, 18 Dec 2025 23:49:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 23:49:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 23:49:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 23:49:12 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 23:49:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 23:49:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e7504fb8b5ca902553810400e8ecf856a5984c36fb7dba7b9d1932f5432750`  
		Last Modified: Thu, 18 Dec 2025 23:52:05 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254154902548782aac7bbe74d12c713d81df39d8b697e905a7ada02053473207`  
		Last Modified: Thu, 18 Dec 2025 23:52:28 GMT  
		Size: 868.9 KB (868948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cb1e707cecbd8b342e8230a81de52b30274d906375bb62c7f6fa905a968ed1`  
		Last Modified: Thu, 18 Dec 2025 23:52:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0565a4b439268fc9d13bb8f0cbe4d925176671b7731ba0d964103b1b8dfca1de`  
		Last Modified: Fri, 19 Dec 2025 03:14:59 GMT  
		Size: 108.7 MB (108730019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbdff487f9f4ca85731291693e74c6626d7b0f07b325a2556057d4ee24896d0`  
		Last Modified: Thu, 18 Dec 2025 23:52:28 GMT  
		Size: 18.8 KB (18782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f6d1b4ee56c2634692a6ca09d95e010948a557484ec289faef583f345d247c`  
		Last Modified: Thu, 18 Dec 2025 23:52:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7345f722ce181178c558639a5ee02fadd1a2551c33faa547bc1066a8255c08a5`  
		Last Modified: Thu, 18 Dec 2025 23:52:28 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ab73ca0341f968b230e90e80bfa2ff3bc02c495b592b4c8f4e2e21e0ee8b9e`  
		Last Modified: Thu, 18 Dec 2025 23:52:08 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed8dba0ce3ae49a6ff138fb10890e85634942b811fdd02dc9ce05ded80f0970`  
		Last Modified: Thu, 18 Dec 2025 23:52:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:d9ee63e2375873a7a3befa779f1fb78283e98a425ab504fd4d0e96bbe7ea6f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.9 KB (642885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38c1a66b46eb565ff8b35e874fd801640c499ca952f07876dcd4c719ff9733a`

```dockerfile
```

-	Layers:
	-	`sha256:6ae7ccbea223d2ec724898f87fd63f6c86285bac9403d6c9e7b1c1cf48d7b8c2`  
		Last Modified: Thu, 18 Dec 2025 23:52:05 GMT  
		Size: 599.7 KB (599703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a76e1cf95eddb207c4ab24210a0ff8bb2f9816124bdc5a10e01c57ba459325a3`  
		Last Modified: Fri, 19 Dec 2025 03:09:03 GMT  
		Size: 43.2 KB (43182 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.23` - linux; s390x

```console
$ docker pull postgres@sha256:ec749c084f1c568b4edf66301f0ea30f65186427a1cbdd8c2aac66a961baa911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120177082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e2d03da4657087c943fed4334fba57a43c50b5520282436b280f19af7d2cc1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:06:27 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 01:06:32 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 01:06:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 01:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 01:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 01:06:32 GMT
ENV PG_MAJOR=18
# Thu, 18 Dec 2025 01:06:32 GMT
ENV PG_VERSION=18.1
# Thu, 18 Dec 2025 01:06:32 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 18 Dec 2025 01:06:32 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 01:11:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 01:11:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 01:11:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 01:11:41 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 18 Dec 2025 01:11:41 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 18 Dec 2025 01:11:41 GMT
VOLUME [/var/lib/postgresql]
# Thu, 18 Dec 2025 01:11:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:11:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 01:11:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 01:11:41 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 01:11:41 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 01:11:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69c5f2050f07a5cb01bb74eff322320d79ef052693ec1bf2e791c3e34ee9ad2`  
		Last Modified: Thu, 18 Dec 2025 01:12:14 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3d39d8e02436f0b019f16e16fc19ff6b779eae84772469808fc5da728fdd6f`  
		Last Modified: Thu, 18 Dec 2025 01:12:26 GMT  
		Size: 897.4 KB (897417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6bb97427b6f31c3b22f870e9da44ec7674b38e9d345bdba0e657a54306f4a7`  
		Last Modified: Thu, 18 Dec 2025 01:12:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c9e342b22362c6025ced5450bf4ef1db32b6a57196ae9c4da1a481308b3abe`  
		Last Modified: Thu, 18 Dec 2025 01:12:33 GMT  
		Size: 115.5 MB (115529157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32abf35c4794f0ad4046c13a6d81222336c7f6b84ffcda9ff3f3580d4b8bd4ec`  
		Last Modified: Thu, 18 Dec 2025 01:12:24 GMT  
		Size: 18.8 KB (18776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea32e6e41a70802fc40ae0a5831e0c8af2fe921814a6ad20d120407ce280a74`  
		Last Modified: Thu, 18 Dec 2025 01:12:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4cd53776f3ca695a415c1a469b846d85b09974ac5eae0761b5246d97827f53`  
		Last Modified: Thu, 18 Dec 2025 01:12:24 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e24d1b441790c16493c7ba2b2d9a0873fe1cbce70ddce85dca7e2647315aee`  
		Last Modified: Thu, 18 Dec 2025 01:12:24 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f79bc4ac9c5a067e1355a580d75b99cd28982844bf10d0ad512f6a3af10697`  
		Last Modified: Thu, 18 Dec 2025 01:12:24 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:e366401797406e758720eca2a08ee15d3eb470f915ab646ed4052c3616c6a43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.8 KB (642773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa2f32469d1287d2e2cc94a6c18bda3d0e3ce92d6210ac67804e3c196ad28c2`

```dockerfile
```

-	Layers:
	-	`sha256:c46d528b16a89a45d7be24a9d9fc2479bf9e4bde86bb6a59e7589c42bac39b3b`  
		Last Modified: Thu, 18 Dec 2025 03:12:01 GMT  
		Size: 599.7 KB (599661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:907c7a97f80a34fa39fdf8350ceb2fdd22e3d25ce9753ad7f48880c84478bb74`  
		Last Modified: Thu, 18 Dec 2025 01:12:17 GMT  
		Size: 43.1 KB (43112 bytes)  
		MIME: application/vnd.in-toto+json
