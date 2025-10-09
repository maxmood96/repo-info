## `postgres:16-alpine3.21`

```console
$ docker pull postgres@sha256:613e8e57e4d7c2b8af4506885267e7fdf7d7ebba131dcf64e3491cdb3e1e76d2
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

### `postgres:16-alpine3.21` - linux; amd64

```console
$ docker pull postgres@sha256:e8fe144850f8576417ba7bcfddb19aa44b3211a13b3d9bb39302d0887e98710c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111773820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e4a71692bf41cd3e579b87522386beffef3a251ed8caef4d1befc7807bd937`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=16
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=16.10
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=de8485f4ce9c32e3ddfeef0b7c261eed1cecb54c9bcd170e437ff454cb292b42
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d1252746d8e855b650dc05e15b4c2ab30ceabbf1fa43dbb92a1e8e20a263db`  
		Last Modified: Wed, 01 Oct 2025 00:34:13 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687174997ec562ff884f3809fa0a088fbf5102982a3626e2cfaa3680f8725e43`  
		Last Modified: Wed, 01 Oct 2025 00:34:14 GMT  
		Size: 915.4 KB (915361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b04b4422d04ce9b355e5e9c92f7f4f0c984fc7f401f53581c28415b175f1b5`  
		Last Modified: Wed, 01 Oct 2025 00:34:14 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426b16c6e2f8dedcfa45feb2dfa55fbfc6380c1ff37e94b477b03920f024ba67`  
		Last Modified: Wed, 01 Oct 2025 00:34:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c5cb3e3d0385d255db07a63c8299ed893e0fc48cd18f35847ad3419c8a4076`  
		Last Modified: Wed, 01 Oct 2025 00:34:26 GMT  
		Size: 107.2 MB (107203662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a23f34f8200d28c275d77fca0b68f0c5b2baa306611a58f383c0eff76d44d02`  
		Last Modified: Wed, 01 Oct 2025 00:34:15 GMT  
		Size: 9.6 KB (9559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdb192789d2f340c1851222e3d4317900e8d1e4749e7481ccf8d567fa8ae87e`  
		Last Modified: Wed, 01 Oct 2025 00:34:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059559d7d0b11bbfb8531a79772a48bf65f3f3fb3e6fe179df4dce3032868262`  
		Last Modified: Wed, 01 Oct 2025 00:34:15 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699232b602d2f162f04942c7fc2457f437403cc033acb387c8be6317f41d8c4b`  
		Last Modified: Wed, 01 Oct 2025 00:34:16 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c440e3ab0fe77771dcbf005b16f6d6ed8ae37e7b4e72751a900f3140efefd23b`  
		Last Modified: Wed, 01 Oct 2025 00:34:16 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:3a2c0b7380a71f6363306b293b4a4114f485dfa67fa1274e577c9e462010a0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.4 KB (642419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2d8043becc6e1a37366ea68bb8206ae534ef3005413be4db78e725dd743dcf`

```dockerfile
```

-	Layers:
	-	`sha256:4f816cf1b600e2639cfa65d9075d44c0d5f917bc186e1229999f1b979b94cb56`  
		Last Modified: Wed, 01 Oct 2025 14:15:02 GMT  
		Size: 598.7 KB (598692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2859b6029c5d301ba5e86846878609b09f4b0b5ab41f7dcc1f4d78795d59806`  
		Last Modified: Wed, 01 Oct 2025 14:15:02 GMT  
		Size: 43.7 KB (43727 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.21` - linux; arm variant v6

```console
$ docker pull postgres@sha256:4e37cf7606606f8e071dacb0037d0045a08b9560d8660cdd0bda37c6dc237e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (89035278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569cc6707706e58ca960c533c1471d80f605ce288a8d30d303ad7f7c76053888`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 30 Sep 2025 18:58:13 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=16
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=16.10
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=de8485f4ce9c32e3ddfeef0b7c261eed1cecb54c9bcd170e437ff454cb292b42
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220a5ba7fecc3d445673a4e4de069e19cc5775c6509a4c9a4f0b033ed996771e`  
		Last Modified: Wed, 08 Oct 2025 22:06:06 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaa4763e47a5d2827e99432a6425a99f49b463d44ebbed3e3fd07ee932583b4`  
		Last Modified: Wed, 08 Oct 2025 22:06:07 GMT  
		Size: 886.1 KB (886097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c2ae2aac99f176accf8dfcaf346aa5cd331ee6a15908e4fbfd0403ce2ddf1d`  
		Last Modified: Wed, 08 Oct 2025 22:06:07 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20246d36b9c95fb7498b6bca1b6df320f152c8b8e878f81e666e7b8ad654a058`  
		Last Modified: Wed, 08 Oct 2025 22:06:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0259e1c6d875701a8b6c67a23e1f4aac892e1f95bc1aa7700e4bc3120930de33`  
		Last Modified: Wed, 08 Oct 2025 22:06:13 GMT  
		Size: 84.8 MB (84766495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d477ffdad292b8323441a0bc2c0b1a36b063081a5e7704a11f6592fec8fc3eba`  
		Last Modified: Wed, 08 Oct 2025 22:06:07 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c584ef966458b57ffb41e1a8d8b7e2f0b0ccdc1002c187742031cf7dd04e9d3`  
		Last Modified: Wed, 08 Oct 2025 22:06:07 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8248201e1a498b73c3fca8d8b19547b0936a078cc5f5494632b9044ad7d41b34`  
		Last Modified: Wed, 08 Oct 2025 22:06:08 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5417650fe6a795dad1a14fcf4470c12019b06abbe39ecab18a2244444bc325`  
		Last Modified: Wed, 08 Oct 2025 22:06:07 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d94e7f58504d5c2d61aed52974f37d0dfa17a18cf091efcadfc7b6f08b585f0`  
		Last Modified: Wed, 08 Oct 2025 22:06:07 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:6f03bd3e61634166b3f993b67c59af8f8af03eba0ea118055b8e2091e9bd71c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 KB (43674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce4eb3673d8630b5f8f9536f2698b3e1521050d919be80deef93dc07cb572295`

```dockerfile
```

-	Layers:
	-	`sha256:eaa6f57d108c7f055175ccca6742c23679ce38c01a6124d391fac569faf648bb`  
		Last Modified: Wed, 08 Oct 2025 23:10:48 GMT  
		Size: 43.7 KB (43674 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.21` - linux; arm variant v7

```console
$ docker pull postgres@sha256:1003d24201b83ffdf996d810a698327708c8a13b3375cf4bc8c0d93866118bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86053890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234098fc61f717d62888ea3514987ac37a1ac3f7ea56a60a0cd8404d716a181a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=16
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=16.10
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=de8485f4ce9c32e3ddfeef0b7c261eed1cecb54c9bcd170e437ff454cb292b42
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5953ca93576fecba22e7812c1b44c493b787d8d30a677b2cf83607e3b980407`  
		Last Modified: Tue, 30 Sep 2025 23:17:17 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9511be8f829e409cf28c5b7fd24891a6ed87bf04337db7281904d2018a88b730`  
		Last Modified: Tue, 30 Sep 2025 23:17:17 GMT  
		Size: 881.7 KB (881732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184c9a67c960d712500786b4087dcd5603b94223b9f98673bd2ad6093ab7e9a5`  
		Last Modified: Tue, 30 Sep 2025 23:17:17 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35fd00935c2df29737d2acd73959d52b52777860e9e1af212a87b8c990b495c`  
		Last Modified: Tue, 30 Sep 2025 23:17:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed59164c8d73c9f634bce77ca345bd8382cf11992d83058acc170a4fe7fd6161`  
		Last Modified: Tue, 30 Sep 2025 23:17:27 GMT  
		Size: 82.1 MB (82058063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004d99b7747d265f45d4dc7c3b030a8ae247dfbe998099d8f4622afbe13532cc`  
		Last Modified: Tue, 30 Sep 2025 23:17:18 GMT  
		Size: 9.6 KB (9559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcaa566670123f4c64864916fc3c940ee38f5a65e85226b3fbf63a9b86374fc`  
		Last Modified: Tue, 30 Sep 2025 23:17:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e037fd6c8367a5514ae8db72a4684a4a22d26717d21bb0db2a158bab483b7fc`  
		Last Modified: Tue, 30 Sep 2025 23:17:18 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73156008dced50e6d660ba7b2e437e9635610c8e960f958f9fd0809c019c0efc`  
		Last Modified: Tue, 30 Sep 2025 23:17:18 GMT  
		Size: 5.9 KB (5925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3230c620057273f4517b32f5fe0de4cfd158a00f852b8d708a36921c2c192ebd`  
		Last Modified: Tue, 30 Sep 2025 23:17:18 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:2de65fb6312dbb3a20fbf86cbda944592582aa273f719b2f8658866a2ab8a9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.6 KB (642601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f48862d2d0ba4886e9f736491cb02bb2dbbca9e6b91a6a37e4d89e9e933dc06`

```dockerfile
```

-	Layers:
	-	`sha256:865df0641e596fe2752ace465039f437e4a00cb3011e69d656399e9542552c65`  
		Last Modified: Wed, 01 Oct 2025 20:14:13 GMT  
		Size: 598.7 KB (598712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d4fd33d3ad88483e0c228f305679469ca62492abe3ae6bfc0d7befe84b344d7`  
		Last Modified: Wed, 01 Oct 2025 20:14:14 GMT  
		Size: 43.9 KB (43889 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:fabb5adcfa99fc6492ee4b4a029f9735500477ec842f4d5bf289b1f655de45e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105386562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb552f4e931af71b5b92034d2aa3e77f94171805a7ed3da3fb2364f5a3f91ef2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 30 Sep 2025 18:58:13 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=16
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=16.10
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=de8485f4ce9c32e3ddfeef0b7c261eed1cecb54c9bcd170e437ff454cb292b42
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb109cb213e6638b47f09a2ea8fd3e878ec3a2880d2b3c451738d359e776401b`  
		Last Modified: Wed, 08 Oct 2025 21:42:07 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1177b333d5b1918e0e5d7b6316c7d43bcf8a06264771c28a93337e4583934560`  
		Last Modified: Wed, 08 Oct 2025 21:42:08 GMT  
		Size: 873.5 KB (873452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1ea8fe461af65418ed9edfd6eeff8e02433e9b330dc897edfff93ecdc694ac`  
		Last Modified: Wed, 08 Oct 2025 21:44:33 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1296073e286fcd6c426da1159e842470b057066e47c20bbcf24c3f0d2fc61b1f`  
		Last Modified: Wed, 08 Oct 2025 21:44:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682616856901d9c63a559f15bbf3a51b9ef97075a7a00acba5df9da65d2827cf`  
		Last Modified: Wed, 08 Oct 2025 21:44:44 GMT  
		Size: 100.5 MB (100503533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262cd68aa014e62242f2256a8e86687e8c13b82f15e11f3ba6dea859d641675f`  
		Last Modified: Wed, 08 Oct 2025 21:44:33 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c9eb24278cad3f71d763b9cc635f1d320f17795446e64055e3c63ff53643c2`  
		Last Modified: Wed, 08 Oct 2025 21:44:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0b6d08f34b838185cd47cba0922bd3714c06f4b2d382e5c354ada2cf23668d`  
		Last Modified: Wed, 08 Oct 2025 21:44:33 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9266810229d8befabd6a1c07eca53996460a481a92c11b1051d13d54f0fd6b`  
		Last Modified: Wed, 08 Oct 2025 21:44:34 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f139f886c79c8b4b896565e182a4771cf9c88886fa809dcc8b9937e8efdf3135`  
		Last Modified: Wed, 08 Oct 2025 21:44:34 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:24021085d6fffdecd3533054b13976933beed63c451fc6e2483d8210916eae63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.6 KB (642650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e822591b77b63d63c1f572e02fddcd7495732c753e96aa683d32e699372ff2c`

```dockerfile
```

-	Layers:
	-	`sha256:6291cb70d992b50bb6f6645ec900032efd38cfe041419720a4c26ef15338eb04`  
		Last Modified: Wed, 08 Oct 2025 23:10:54 GMT  
		Size: 598.7 KB (598724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8756b8328ca8d6a1905667f336e855dcc5022065ac56f15e083740a4eabd01ef`  
		Last Modified: Wed, 08 Oct 2025 23:10:54 GMT  
		Size: 43.9 KB (43926 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.21` - linux; 386

```console
$ docker pull postgres@sha256:95ff43faed5cb7d58f7d82ef6e68f899569b560ca94079ec69cdb57327b66e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115615391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8d98b74190c9c4158b272bfbc8bd3dea5e1473557587411b7ab842c19bac45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 30 Sep 2025 18:58:13 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=16
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=16.10
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=de8485f4ce9c32e3ddfeef0b7c261eed1cecb54c9bcd170e437ff454cb292b42
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57bd8a3b5bafa293ff5530a51f0377bebe904d37fbb0f8e5303151ce89b8772`  
		Last Modified: Wed, 08 Oct 2025 21:39:09 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d3db4d672936f0f20e609540b615084cad3a5f40d0934a22030e2583196caa`  
		Last Modified: Wed, 08 Oct 2025 21:39:09 GMT  
		Size: 890.6 KB (890606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93bf9c0780150598e3ce65a17022a211964061ddb3196cd825db79f8ee8c781`  
		Last Modified: Wed, 08 Oct 2025 21:39:09 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83182d1cb8b626774a52a5edcb2b2142389d1dbc32d223faf15b256b8a2e5f86`  
		Last Modified: Wed, 08 Oct 2025 21:39:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8879f9f244eb85fd9cd727c0afda8300c246db4c704a47144aee89a9c6848ab8`  
		Last Modified: Wed, 08 Oct 2025 21:39:05 GMT  
		Size: 111.2 MB (111242851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fcb61fd361368d0d3b63fcb0e540181662718aa098e778308e1ecfa177c6c0`  
		Last Modified: Wed, 08 Oct 2025 21:39:09 GMT  
		Size: 9.6 KB (9563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe552a93d0518f5f53bbff90ee135004044800389f84e90abb149b8655d182b`  
		Last Modified: Wed, 08 Oct 2025 21:39:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c927c3d3aa9ed9b83aa22f38ab16cadccd30439d4fe863d8589bb1cc93c7ab3`  
		Last Modified: Wed, 08 Oct 2025 21:39:09 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ffac222a3694ea1b188e0d2a0dd865d36357f19c004e4ab81fb8e7c2151db9`  
		Last Modified: Wed, 08 Oct 2025 21:39:09 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713dea21cf7ad767b87af746cfdefed2c78d335cb863ac0a1bb38a6bb9ba0e01`  
		Last Modified: Wed, 08 Oct 2025 21:39:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:669de73f324f1d72c9425001ec2986a35444b04ca6ff0b3823152b714f5986fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.4 KB (642364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f175fe0c6ef22e762ab6c743d1ae4f17f2e4522c9683753b18755217fce3071`

```dockerfile
```

-	Layers:
	-	`sha256:6bb8fa689ea4bb416eb44a644e67afe87d814939bf75c8382c55566e576953bf`  
		Last Modified: Wed, 08 Oct 2025 23:10:58 GMT  
		Size: 598.7 KB (598677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:422dbe7f5dcc5650be5e70945f36e9ef3fa35aa7f5649a85280d4c1a4e6b16fd`  
		Last Modified: Wed, 08 Oct 2025 23:10:59 GMT  
		Size: 43.7 KB (43687 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.21` - linux; ppc64le

```console
$ docker pull postgres@sha256:09732c70a7b8c8a2a87a92628e83927b9ac2856b18ecf89f2182de9388bcd310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95398452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3810ba1c6b006ffc0778a9c197b952f7f7a70c2018b51d0b030850b3b5803b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=16
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=16.10
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=de8485f4ce9c32e3ddfeef0b7c261eed1cecb54c9bcd170e437ff454cb292b42
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747bf6778b8e7ed31d4743686f1f50485c5c074620417743c59a087cdb5f9186`  
		Last Modified: Wed, 01 Oct 2025 08:36:58 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ded0eec492104ecd2eae20f50bf37ad15ee8c2428edc86b79a41ad80e9addb`  
		Last Modified: Wed, 01 Oct 2025 08:36:58 GMT  
		Size: 873.8 KB (873763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcbb7374b33366d8cc37a51cf30a09f597c947f160ec3c072a6c438ddf6707d`  
		Last Modified: Wed, 01 Oct 2025 08:59:08 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe80ba2325ccbca20c2bc91de1403de3d608e89a78544898eba2cf99687aca8`  
		Last Modified: Wed, 01 Oct 2025 08:59:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c53cf3e2fc3ee6f809ddbef3aa05f0c301c3b8ad954193f640db6ee7450bcd2`  
		Last Modified: Wed, 01 Oct 2025 21:33:22 GMT  
		Size: 90.9 MB (90938324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891aa1fc9d2624589cd640b3deb3db9e37b2db25fedb187978ad52a05c725573`  
		Last Modified: Wed, 01 Oct 2025 08:59:14 GMT  
		Size: 9.6 KB (9563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cecdab2f003a8b72035e51b84fc572c43ae6b35599d38b233d6fd21a854c066`  
		Last Modified: Wed, 01 Oct 2025 08:59:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d10dda17edb5727a34b3ac8b47de2235ac1a00b331d110753472bff17cf374`  
		Last Modified: Wed, 01 Oct 2025 08:59:22 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa563a04a7bf732f64142ed4fa8835174d4ecd411853d5f72a5fcba88a9d6d7`  
		Last Modified: Wed, 01 Oct 2025 08:59:25 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8855421d689be1943a97a88b334df0b6f506b8cb6042cfe5b74d216b2c29512`  
		Last Modified: Wed, 01 Oct 2025 08:59:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:65cdb8dc6aac284d792c0c21c2132b5ba6ea6cff04d2afb80819330fc794f913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.9 KB (638870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba8c6aba2a08ea92f6462d3e458b29ad2763c35b8e85f4ec25d0a6907724b37`

```dockerfile
```

-	Layers:
	-	`sha256:e736c353568ed94787de7f959cac11f48369beb15a745b1c39b06a19e6622a37`  
		Last Modified: Wed, 01 Oct 2025 20:14:23 GMT  
		Size: 595.1 KB (595101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f2dc5919222414088109a4a5ffe1c68dc711beb0d5abf07b994ff6e88c54390`  
		Last Modified: Wed, 01 Oct 2025 20:14:24 GMT  
		Size: 43.8 KB (43769 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.21` - linux; riscv64

```console
$ docker pull postgres@sha256:00df40f4a82a96145d398477c326b50ebbddfcaca7ef3b8b08d81a0ff9f93174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111428143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f744b7ca0b24c5e96c260282d19658da3974e8672b1ec4a3cbab375eaf44805`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=16
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=16.10
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=de8485f4ce9c32e3ddfeef0b7c261eed1cecb54c9bcd170e437ff454cb292b42
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f442f14b9fc184be7b5b23f9b5362306d14b41b75f0fc847fcc5851ab3402e5`  
		Last Modified: Wed, 24 Sep 2025 00:47:22 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a806fe08f5cb13a300574c46c89d7d784c57ea301fece231af5a28695589eac`  
		Last Modified: Wed, 24 Sep 2025 00:47:23 GMT  
		Size: 860.8 KB (860848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447da1560e7579310046d88af470ba2bfe8a6d5d8e228e2068d32f9409c44707`  
		Last Modified: Wed, 24 Sep 2025 08:50:53 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19719383b23bb55e69b9acb371535c6a6bcae9dcbb54cebd17541e6b8e59b49`  
		Last Modified: Wed, 24 Sep 2025 08:50:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49331f4db22eff5848f893eac19dc6a36d38619b35c7e1fb1fbb45828d21d362`  
		Last Modified: Thu, 02 Oct 2025 18:44:08 GMT  
		Size: 107.2 MB (107200960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf6f221ccd2a40111a800c2c02b305466dbd58137cd147e3c65f7f74b648ea9`  
		Last Modified: Thu, 02 Oct 2025 18:44:00 GMT  
		Size: 9.6 KB (9568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfed4f67cfd5f5693670de8b50c3a8f64babbaa8f87cfc260d87ad3d18d72d2`  
		Last Modified: Thu, 02 Oct 2025 18:43:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922bdced5d233633c167f8a8aa6705e7d713984390bcddb2f7d34522232d842b`  
		Last Modified: Thu, 02 Oct 2025 18:44:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e9be18e026715b14230a5a4d50785609976383a56f246adb5e4bba54359cfc`  
		Last Modified: Thu, 02 Oct 2025 18:44:00 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a919b946f2b8eef6e6d9dc4665562468ae621f0ea8d43969edf08f6ffda131`  
		Last Modified: Thu, 02 Oct 2025 18:44:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:f81530ca8df06c1ca943e69ea96a4390fe0b4c485e226bbc7bfad05e8bd9f8b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.5 KB (640533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71f9e25f2696360cfe33bc7f830ecdda6989cb5696b0ae4691e21d3f540d4f3`

```dockerfile
```

-	Layers:
	-	`sha256:570b621815acc7259c255636cdeaff27dea040fb86a4940abbefd4bd3ee6da97`  
		Last Modified: Thu, 02 Oct 2025 20:08:47 GMT  
		Size: 596.8 KB (596759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d018a06da1b322ad40c8e7156599e6afb6c9b3bb747e4ec0e742562fc24c3a67`  
		Last Modified: Thu, 02 Oct 2025 20:08:48 GMT  
		Size: 43.8 KB (43774 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.21` - linux; s390x

```console
$ docker pull postgres@sha256:5c9c039415d5c937f642416ebc1f8d4c6a064aa843f8e399d8eee0ae044e1338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120111250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a386d3e3249e41c9178ffcb0420c0f568eedf82e36ed80d0bcdf444557353180`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=16
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=16.10
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=de8485f4ce9c32e3ddfeef0b7c261eed1cecb54c9bcd170e437ff454cb292b42
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3a0b3e42a00821c504172afe5ad33497b04821fb945d8f1762c22b804de062`  
		Last Modified: Tue, 23 Sep 2025 22:00:10 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfde9cde752b53d44f7ef28a4eaabe5d98c6054f6df4adb3d525fe6d7846494`  
		Last Modified: Wed, 01 Oct 2025 04:51:03 GMT  
		Size: 891.2 KB (891242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4fc88dd289be74ba2ca2ead2356391f5695518a0bc2bbbc86b46e2db34fe01`  
		Last Modified: Wed, 01 Oct 2025 05:08:04 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b672fc6af4622dc19a1e29bc041de271a18f9da1c4f630ee343bbf6d54a0301`  
		Last Modified: Wed, 01 Oct 2025 05:08:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd45e3286165c5e1509c18961d6198259bd07aa2abea664790f261918f32a57e`  
		Last Modified: Wed, 01 Oct 2025 05:08:12 GMT  
		Size: 115.7 MB (115740671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e6a35bc56ade7c9eaa135ab6bc84c3fa5756fe72a43468f942158c31f3c3e1`  
		Last Modified: Wed, 01 Oct 2025 05:08:04 GMT  
		Size: 9.6 KB (9567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5580c3141a93ceef91a4490baaaab1fd9bfceb1ee8586fb207c1fac9cc998ec9`  
		Last Modified: Wed, 01 Oct 2025 05:08:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc38d014fa2e63872e1e9815e8bf03a4b9b4845ee49f6713befe503d00f421d`  
		Last Modified: Wed, 01 Oct 2025 05:08:04 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204aa371926a20f77bd496764bf977f49bf5c72c32453bf279c46f86edaad819`  
		Last Modified: Wed, 01 Oct 2025 05:08:04 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bf71b2d5ed92fe9a9f721b9e7339d59f225d10e789c45226ba5a5edd78b68a`  
		Last Modified: Wed, 01 Oct 2025 05:08:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:0c46d2a08bfef2731928466648ae1ee163eef226ae475971fe36d2fa458e3bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.5 KB (640466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d4059e077feb0d761e8b35e4c8ca27b7aff1e7926215ea81dc99eb367876b5`

```dockerfile
```

-	Layers:
	-	`sha256:1a1a1f778f3609d9807e2b5f214d3d214b2e9a9908d073b2da767aeb310604a3`  
		Last Modified: Wed, 01 Oct 2025 20:14:29 GMT  
		Size: 596.7 KB (596741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f49adc9b6f53a03d893f4be34b8c4505c2b1e3b0432ed1f90e6026c375de3a`  
		Last Modified: Wed, 01 Oct 2025 20:14:30 GMT  
		Size: 43.7 KB (43725 bytes)  
		MIME: application/vnd.in-toto+json
