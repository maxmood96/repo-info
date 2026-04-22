## `postgres:17-alpine3.22`

```console
$ docker pull postgres@sha256:08e9cdef3011222e88cd3ccfce73fad0f57f2cb204ba43fba8d7a2ae52d8fd4c
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

### `postgres:17-alpine3.22` - linux; amd64

```console
$ docker pull postgres@sha256:ec5170db1294cd3707b05eb6942104c4c77f37ba61258f2d51617bc46f93bce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110640667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7942968c7471cb974cb71623cb161434941a15862a06c4d296dda406fb4e79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:07:02 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 21 Apr 2026 23:07:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:07:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:07:04 GMT
ENV LANG=en_US.utf8
# Tue, 21 Apr 2026 23:07:04 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Apr 2026 23:07:04 GMT
ENV PG_MAJOR=17
# Tue, 21 Apr 2026 23:07:04 GMT
ENV PG_VERSION=17.9
# Tue, 21 Apr 2026 23:07:04 GMT
ENV PG_SHA256=3b9a62538a8da151e807a3ddb1198e8605f2032544d78f403ae883d27ecf1ee4
# Tue, 21 Apr 2026 23:07:04 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:09:19 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:09:19 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:09:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:09:19 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Apr 2026 23:09:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 21 Apr 2026 23:09:19 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 21 Apr 2026 23:09:19 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:09:19 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:09:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:09:19 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:09:19 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:09:19 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fc43500b9c0aa4ca7bffe11775f9f1dd68899c1a766cfd9392e619f3d119b0`  
		Last Modified: Tue, 21 Apr 2026 23:09:34 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af34d3059cd64648dc47f18ecc930c810eedc94d5cafdb78f816e8cbcd0777fb`  
		Last Modified: Tue, 21 Apr 2026 23:09:34 GMT  
		Size: 917.4 KB (917428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfe108fb11125d996ea6725c094eed791b5ce472a269976ff153a660683ccb3`  
		Last Modified: Tue, 21 Apr 2026 23:09:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857aa751c49f6cddb75a7f471e7ca24defa744922521d125db872675289cae4d`  
		Last Modified: Tue, 21 Apr 2026 23:09:37 GMT  
		Size: 105.9 MB (105897437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e92a4d0f019a3bc42027a57665f6d4eb356689e589cc7bc29d7b51693c5178`  
		Last Modified: Tue, 21 Apr 2026 23:09:35 GMT  
		Size: 9.9 KB (9949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be6cca1a31fd960c6f6fdd0813dcbbd90229687f5c06c95eb5f50cecb9652ca`  
		Last Modified: Tue, 21 Apr 2026 23:09:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9e3e671fc35f47fd5b96ab9ea205ba306ad1fc017343ef86c146e814e9273e`  
		Last Modified: Tue, 21 Apr 2026 23:09:36 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2514879cb7b7c4ecb76e05985cd2ad74902248895baf8c4459ef212f5c348cb5`  
		Last Modified: Tue, 21 Apr 2026 23:09:37 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f709bce45fc2e11363e94621a4b3a7bfb9732f02a1afb949ae749da80ee79906`  
		Last Modified: Tue, 21 Apr 2026 23:09:37 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:90bbb8fd409e30550771660fa37d19ccb56e98ba8587212575497f20ce48aa42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.4 KB (637369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6e2a423e76ce7fae9b40da10b614f74126e59051a3531a6f239d87dd6622b2`

```dockerfile
```

-	Layers:
	-	`sha256:bcca201488843feab5fae9eafb9a0037b2d5c550823f8cd496232d0d5d90fa93`  
		Last Modified: Tue, 21 Apr 2026 23:09:34 GMT  
		Size: 596.3 KB (596311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ad8b1f4b3913c08c970f45774eb573be5c97b6e74e6d438529a1bc3dda01f7e`  
		Last Modified: Tue, 21 Apr 2026 23:09:34 GMT  
		Size: 41.1 KB (41058 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:faf382479b134e4154b9c260daa10fb1d4148e5a4169388ddb0ed640674e95a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90145419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7caad7de80d184ef8cc8a451443deeb1ea60da023c6904d02ec19e785a34d42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:12:42 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 21 Apr 2026 23:12:46 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:12:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:12:46 GMT
ENV LANG=en_US.utf8
# Tue, 21 Apr 2026 23:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Apr 2026 23:12:46 GMT
ENV PG_MAJOR=17
# Tue, 21 Apr 2026 23:12:46 GMT
ENV PG_VERSION=17.9
# Tue, 21 Apr 2026 23:12:46 GMT
ENV PG_SHA256=3b9a62538a8da151e807a3ddb1198e8605f2032544d78f403ae883d27ecf1ee4
# Tue, 21 Apr 2026 23:12:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:15:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:15:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:15:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:15:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Apr 2026 23:15:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 21 Apr 2026 23:15:55 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 21 Apr 2026 23:15:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:15:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:15:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:15:55 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:15:55 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:15:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fbe5b39c2edfcd75c4c1128ebd6e6d6fdc35f085fcd2ae62f5ea1b0cd7e2ef`  
		Last Modified: Tue, 21 Apr 2026 23:16:06 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b6f641f47766c4f06a99ee8a58cff474a787ff662a290039b4733be591df31`  
		Last Modified: Tue, 21 Apr 2026 23:16:06 GMT  
		Size: 885.1 KB (885149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061d7e4e2367139dda5ed63329546d24ba888b438093123697801504b643f614`  
		Last Modified: Tue, 21 Apr 2026 23:16:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8d215861dfaf1f82299b2125a53b62b8f7d3103a868ba9e9c9dc045ad2fd24`  
		Last Modified: Tue, 21 Apr 2026 23:16:08 GMT  
		Size: 85.7 MB (85735270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1a2486532ddb206b82eda85eb4e538e39e91e0edf813aa5c7921428c242bec`  
		Last Modified: Tue, 21 Apr 2026 23:16:07 GMT  
		Size: 10.0 KB (9951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5980a98d373ebba3a0f2b72785e7423f47d7c417022399e78675b4016fb98a`  
		Last Modified: Tue, 21 Apr 2026 23:16:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d491fff6772f59e6741e8e65192cc788eca0a1574c11f9e38d5096f2d44e65e`  
		Last Modified: Tue, 21 Apr 2026 23:16:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636561050b24165505bf961c2e52938771c6fcd220344421b2e9035930c72521`  
		Last Modified: Tue, 21 Apr 2026 23:16:08 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c472843e3c7deb8e15a45814ab171553aab41c286ac1849b4cd1ad952f6fcc4b`  
		Last Modified: Tue, 21 Apr 2026 23:16:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:9e692e196bf0f5cfa09e668e22c21913d6239fa00d0f5f4c20ca2f4bfce50e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 KB (40991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124ed44af7ae6afd59bfed14ddef23fce810a65ed6ea8ca841fc8820605c87cb`

```dockerfile
```

-	Layers:
	-	`sha256:159a8138409169b8dbcbf4b39047e30f717101a8acbd14062a4b48e80811c45d`  
		Last Modified: Tue, 21 Apr 2026 23:16:06 GMT  
		Size: 41.0 KB (40991 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:3d005f2d45e7651c04b96440614cdf3002c8839cf2ed6efe8b2853368933711a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85393291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a52a3f0e66af7bbc4fab8efdb5be964f06a34cca92b57d3a04edd54edfc23f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:31:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 21 Apr 2026 23:31:20 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:31:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:31:20 GMT
ENV LANG=en_US.utf8
# Tue, 21 Apr 2026 23:31:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Apr 2026 23:31:20 GMT
ENV PG_MAJOR=17
# Tue, 21 Apr 2026 23:31:20 GMT
ENV PG_VERSION=17.9
# Tue, 21 Apr 2026 23:31:20 GMT
ENV PG_SHA256=3b9a62538a8da151e807a3ddb1198e8605f2032544d78f403ae883d27ecf1ee4
# Tue, 21 Apr 2026 23:31:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:34:21 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:34:21 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:34:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:34:21 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Apr 2026 23:34:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 21 Apr 2026 23:34:21 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 21 Apr 2026 23:34:21 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:34:21 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:34:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:34:21 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:34:21 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:34:21 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9723b2e5e6b036a80fb51317a33e7a21f59d8bd65fd87a13abcbf9fc7a74c325`  
		Last Modified: Tue, 21 Apr 2026 23:34:33 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f49589de7f75e392964722651ba63f2c90517ec1e916da0d3ceda39b09983e`  
		Last Modified: Tue, 21 Apr 2026 23:34:33 GMT  
		Size: 885.1 KB (885150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cd50ccc878db3a5d51a29e6587fcb35db332342c1422d85023672920b53be7`  
		Last Modified: Tue, 21 Apr 2026 23:34:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53482e9011de9809b1184728d770545e310b70a253ede76086990e6513e8d882`  
		Last Modified: Tue, 21 Apr 2026 23:34:35 GMT  
		Size: 81.3 MB (81264697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8365373b2f6611e755820a33551053e095e6dd79f7909f1456096afa0b051408`  
		Last Modified: Tue, 21 Apr 2026 23:34:34 GMT  
		Size: 10.0 KB (9951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee4c82f65371d2809bf17bddc5b91b6d7fdf50aa6a34e3a2e5915aeab93b511`  
		Last Modified: Tue, 21 Apr 2026 23:34:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d87473c7d90166acf3957070ab70cc05b8db1a092a9f93f5de47fb87628908`  
		Last Modified: Tue, 21 Apr 2026 23:34:34 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9808eb787a1374fcce66e0b3680396aa06885961977988020cb2f539064743c`  
		Last Modified: Tue, 21 Apr 2026 23:34:35 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04308fcb2db6d057d160596dcd4861f0cb6f3bad0f0f7ef01f1ac44dcb809d8`  
		Last Modified: Tue, 21 Apr 2026 23:34:36 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:394f4d1796c12b44fb12839cc56a19af6ba7a8c678fc7c44e5ceb00887fc969d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.5 KB (637538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0822d4912b6bac469154b275a025c94457ea62727a0855dbcb19fe2a34a0ea55`

```dockerfile
```

-	Layers:
	-	`sha256:48c8fbf50c659e779538fba3d7667fb1e7e66f8457f48087d1efdbb0c760acba`  
		Last Modified: Tue, 21 Apr 2026 23:34:33 GMT  
		Size: 596.3 KB (596331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:110bbf42bbd04a690fec0a934112c52882302e079598e4feca4c476aa713c648`  
		Last Modified: Tue, 21 Apr 2026 23:34:33 GMT  
		Size: 41.2 KB (41207 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:f2b1fec3c89dc28c24edf25bb3ce7bef252fd18b356e99fbf0514ad6c764259e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106583912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402aafa14e3358e9f51d52b27ff503fb3ea4dc849b14babc0a1d95ce6a81de77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:08:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 21 Apr 2026 23:08:15 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:08:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:08:15 GMT
ENV LANG=en_US.utf8
# Tue, 21 Apr 2026 23:08:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Apr 2026 23:08:15 GMT
ENV PG_MAJOR=17
# Tue, 21 Apr 2026 23:08:15 GMT
ENV PG_VERSION=17.9
# Tue, 21 Apr 2026 23:08:15 GMT
ENV PG_SHA256=3b9a62538a8da151e807a3ddb1198e8605f2032544d78f403ae883d27ecf1ee4
# Tue, 21 Apr 2026 23:08:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:10:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:10:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:10:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:10:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Apr 2026 23:10:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 21 Apr 2026 23:10:56 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 21 Apr 2026 23:10:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:10:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:10:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:10:56 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:10:56 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:10:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3538db95fa383b0676cd7f1c1e5e291ec5d8d01b54b04cc0a941396308c95e0`  
		Last Modified: Tue, 21 Apr 2026 23:11:11 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dca38013d111cb30f5e5d607ff9920adcbefd23399025cb617833fd6031bd80`  
		Last Modified: Tue, 21 Apr 2026 23:11:11 GMT  
		Size: 873.1 KB (873131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee78c17ff5e6e7bc9f31ec57b2591e371087e964f4e791bb520133a5f6de7c5`  
		Last Modified: Tue, 21 Apr 2026 23:10:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f802b9b84c037b64c15f98bc6358d3383d70608566df6c020ab741aec4f35404`  
		Last Modified: Tue, 21 Apr 2026 23:11:13 GMT  
		Size: 101.6 MB (101551277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f4b0cdad3b4026b24ccdaccc3b196b31240af69375feabccdf605785bca586`  
		Last Modified: Tue, 21 Apr 2026 23:11:12 GMT  
		Size: 9.9 KB (9948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9070cee83bcd909c40cf1448b8ddd6d9724bb0da8926369c3a32ba11651cf68b`  
		Last Modified: Tue, 21 Apr 2026 23:11:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7b620f9c10b4a7617101b7c6674880958286e1500819a3566d3a88e38f03df`  
		Last Modified: Tue, 21 Apr 2026 23:11:12 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b23643e7e57ec07e54c3f320ff7a43421a193f7296a48e7dda6fc2db71c2ae`  
		Last Modified: Tue, 21 Apr 2026 23:11:13 GMT  
		Size: 6.1 KB (6094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15569006e431df2622385c266edeea4d05a26241b789ca6da5015f1641b70dc`  
		Last Modified: Tue, 21 Apr 2026 23:11:13 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:a6548247f3520a6bd31a204159692fd7f259789f52bf416f20c902799c0b4458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.6 KB (637586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7bb8b41a6b7acea1aa88bcaa5ec679394fd8ebe26ace80b13dd9c6ae9493707`

```dockerfile
```

-	Layers:
	-	`sha256:28d5f77aef15092d0c338f7d9c6e3bd84abed100d5556c1dba6952c352da395e`  
		Last Modified: Tue, 21 Apr 2026 23:11:11 GMT  
		Size: 596.3 KB (596343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55a2944b254a71b3da0f94308cc6f316dce1e347dc5fe19e3f9d5ffe29a96892`  
		Last Modified: Tue, 21 Apr 2026 23:11:11 GMT  
		Size: 41.2 KB (41243 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:fdaf4dbc94686b063e3edf3ea55eaf1e8aa783cfd5a151e368f4e499a6643869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116916123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620f3a538bc8c62817c39bd53921b98622d7b92a5a8d4dcba7d57da734a02c97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:12:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 21 Apr 2026 23:12:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:12:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:12:16 GMT
ENV LANG=en_US.utf8
# Tue, 21 Apr 2026 23:12:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Apr 2026 23:12:16 GMT
ENV PG_MAJOR=17
# Tue, 21 Apr 2026 23:12:16 GMT
ENV PG_VERSION=17.9
# Tue, 21 Apr 2026 23:12:16 GMT
ENV PG_SHA256=3b9a62538a8da151e807a3ddb1198e8605f2032544d78f403ae883d27ecf1ee4
# Tue, 21 Apr 2026 23:12:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:14:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:14:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:14:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:14:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Apr 2026 23:14:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 21 Apr 2026 23:14:57 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 21 Apr 2026 23:14:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:14:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:14:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:14:57 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:14:57 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:14:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b2ca777c35411255c56a068bfe10d651981fedca4480e030410737d522ad68`  
		Last Modified: Tue, 21 Apr 2026 23:15:13 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c08975bf3b2f7bee36a98391000214591d14dd5a9cafe87d7809e5611dcc74a`  
		Last Modified: Tue, 21 Apr 2026 23:15:13 GMT  
		Size: 889.7 KB (889745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672dfa671c2259a24134c5967f59c75de1b4d9d86cde5ea5dfde56eade9c563a`  
		Last Modified: Tue, 21 Apr 2026 23:15:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9669426aa26da591111d19c517a21a2e76449376b8efc4e7fed7a9287b0b32`  
		Last Modified: Tue, 21 Apr 2026 23:15:19 GMT  
		Size: 112.4 MB (112384042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dc132bf8a798826c4204cc40f79527f1e2598635ee1240684c533d7d3fa149`  
		Last Modified: Tue, 21 Apr 2026 23:15:15 GMT  
		Size: 9.9 KB (9950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700e03c8dba1f7f6866a75e0bf522278d4b5277c41c78c9ee5c0a91af663e74d`  
		Last Modified: Tue, 21 Apr 2026 23:15:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349533e9e0375e2fea75c72fb03c35e7e4a170c22c5a0b6c76cd7e40a4588d85`  
		Last Modified: Tue, 21 Apr 2026 23:15:15 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b930444bee0028a9c2581b7bf3ccbf56c19ca3e778966b76d286bfff43562d9d`  
		Last Modified: Tue, 21 Apr 2026 23:15:16 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caca5d0192d7d68808b709ab8d2b1149b91467279713a5be20b0232eb466ad5d`  
		Last Modified: Tue, 21 Apr 2026 23:15:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:2a23a1474bb79625bab70f096fd3f75727067f00f00ddce13bf24a038c719392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.3 KB (637317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39cf22b671dd210968389610cfc4404f3940e0a380fb1bf52d96f4f0019f5106`

```dockerfile
```

-	Layers:
	-	`sha256:eee947b650f5e2c8c2e5327312e51ea387e5c90132daccf219a8999d7b899237`  
		Last Modified: Tue, 21 Apr 2026 23:15:13 GMT  
		Size: 596.3 KB (596296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ddd45cc654dddfaf22de1c92f1b0d5cfe66d94d22276c0ee9cf5d4f0c6ac74f`  
		Last Modified: Tue, 21 Apr 2026 23:15:13 GMT  
		Size: 41.0 KB (41021 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:2cea8e485b0d56184be5d60ac5ed346f67e23910bf3802563b31b3e8299ff0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94475984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9ee8446794736a24d114b15965efa7b0cefc1fe6e8e43da028710003af7f17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:55:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 17 Apr 2026 00:56:01 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Apr 2026 00:56:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Apr 2026 00:56:01 GMT
ENV LANG=en_US.utf8
# Fri, 17 Apr 2026 00:56:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 00:56:01 GMT
ENV PG_MAJOR=17
# Fri, 17 Apr 2026 00:56:01 GMT
ENV PG_VERSION=17.9
# Fri, 17 Apr 2026 00:56:01 GMT
ENV PG_SHA256=3b9a62538a8da151e807a3ddb1198e8605f2032544d78f403ae883d27ecf1ee4
# Fri, 17 Apr 2026 00:56:01 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 17 Apr 2026 01:00:34 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 17 Apr 2026 01:00:35 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 17 Apr 2026 01:00:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 17 Apr 2026 01:00:35 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 17 Apr 2026 01:00:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 17 Apr 2026 01:00:35 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 21 Apr 2026 23:45:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:45:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:45:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:45:32 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:45:32 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:45:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994fd3b166293e4617ca5472a952e8dc21082efd9682a43943df39ebcf544ae4`  
		Last Modified: Fri, 17 Apr 2026 01:01:06 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2b60bc8e7f425f63f0830c9466a974ba3e426f197d170fb82acc065521ab50`  
		Last Modified: Fri, 17 Apr 2026 01:01:06 GMT  
		Size: 878.3 KB (878310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e352e777c9beceff0496bb0d290e171684587a097a3b2f1bba1c67b4c3e3b13f`  
		Last Modified: Fri, 17 Apr 2026 01:01:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905aa4b1ce0d437fe4c59ea1966233a86a55e4fcf6fc3d8664d2823faa2cb1d8`  
		Last Modified: Fri, 17 Apr 2026 01:01:13 GMT  
		Size: 89.8 MB (89843387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4d9ee76288b50549199a8ff5c7874b55f0c1afeee53794578bc7c2f67556dd`  
		Last Modified: Fri, 17 Apr 2026 01:01:09 GMT  
		Size: 10.0 KB (9956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df97b8d9df062d2050f40a66545237444b09b309ed353e28841f9881f298bc34`  
		Last Modified: Fri, 17 Apr 2026 01:01:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a184eeb3d4947f5e82584eff4090d6d8083dc2f985cef60c4e254d29e7448a43`  
		Last Modified: Fri, 17 Apr 2026 01:01:10 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f095c9d9e2258aab454fce225755ac1efb408b6e9b09c1192e9a0ead7b0ad9`  
		Last Modified: Tue, 21 Apr 2026 23:45:49 GMT  
		Size: 6.1 KB (6103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107a54938a00611e271497fd63dc6624b3a4900f62a555e03ec583c3d1d563e3`  
		Last Modified: Tue, 21 Apr 2026 23:45:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:e346e7e92616899f40807ca4c196a0298218db510a156dc5d6aeadf162389d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.8 KB (633818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0294e88384bf7b845045e1051adf79eea6132fee45d694a4e0e29ee0eebba4`

```dockerfile
```

-	Layers:
	-	`sha256:9625984e2a3a94e678697f78d42fb4902d88e826cf1c283286b35e50a8361229`  
		Last Modified: Tue, 21 Apr 2026 23:45:49 GMT  
		Size: 592.7 KB (592720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6af913ff09a4882bac373ccc8df80870b9ec8e3507545978c258b0ef0792708`  
		Last Modified: Tue, 21 Apr 2026 23:45:49 GMT  
		Size: 41.1 KB (41098 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:ca4cb860a4d4f4b48937e5ba815cc634bb7671f62863ab6f0692955dc30f4218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110719105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1b1b816a82196f59a0f0e269457d713a57934e7977d1d79c468eddc06cd753`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Apr 2026 22:19:29 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 18 Apr 2026 22:19:41 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 22:19:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 22:19:41 GMT
ENV LANG=en_US.utf8
# Sat, 18 Apr 2026 22:19:42 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 18 Apr 2026 22:19:42 GMT
ENV PG_MAJOR=17
# Sat, 18 Apr 2026 22:19:42 GMT
ENV PG_VERSION=17.9
# Sat, 18 Apr 2026 22:19:42 GMT
ENV PG_SHA256=3b9a62538a8da151e807a3ddb1198e8605f2032544d78f403ae883d27ecf1ee4
# Sat, 18 Apr 2026 22:19:42 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sun, 19 Apr 2026 00:05:50 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sun, 19 Apr 2026 00:05:51 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sun, 19 Apr 2026 00:05:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sun, 19 Apr 2026 00:05:51 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sun, 19 Apr 2026 00:05:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Sun, 19 Apr 2026 00:05:52 GMT
VOLUME [/var/lib/postgresql/data]
# Sun, 19 Apr 2026 00:05:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sun, 19 Apr 2026 00:05:53 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sun, 19 Apr 2026 00:05:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Apr 2026 00:05:53 GMT
STOPSIGNAL SIGINT
# Sun, 19 Apr 2026 00:05:53 GMT
EXPOSE map[5432/tcp:{}]
# Sun, 19 Apr 2026 00:05:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587d8e2fd99fe429bf8f22467e93aa876a5641cf7de4fb04ba99bc68a0de695d`  
		Last Modified: Sat, 18 Apr 2026 23:12:22 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a506d334faeab2227b02d175475320187eefeaba57ea193e2009ba29e541869c`  
		Last Modified: Sat, 18 Apr 2026 23:12:22 GMT  
		Size: 865.7 KB (865729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096e923fa3664133bf08c68edc7653025b0c8faa5cc2f2a2525e7e47b2c487dd`  
		Last Modified: Sat, 18 Apr 2026 23:12:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26baac16757234dfaa52c5e612415762c726cc2a5d54152bc89f7e4600a2ffba`  
		Last Modified: Sun, 19 Apr 2026 00:08:59 GMT  
		Size: 106.3 MB (106315128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac605b9786c6d5adbd95d02e47a76eef577c07d76a807c2f44946285fd597402`  
		Last Modified: Sun, 19 Apr 2026 00:08:43 GMT  
		Size: 10.0 KB (9959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994f82b7978b91f0d3e3008cea8541b6b818de194b9cee4e07e444d528131af5`  
		Last Modified: Sun, 19 Apr 2026 00:08:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc6c52d25786b6bcb73100c24f00802bf42a1c9a6e24eb9aa58e888fb869784`  
		Last Modified: Sun, 19 Apr 2026 00:08:43 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e987edfcacccd942c72ba04b393e497a216701bbbe0cbefaea8e905ab9d6e29a`  
		Last Modified: Sun, 19 Apr 2026 00:08:45 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d339eb3cc71439886b464f680c8e61c0348a27bd4c5f05729ea00470c68526b6`  
		Last Modified: Sun, 19 Apr 2026 00:08:45 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:e9aa9ccc45c228acf9b64c99e8b74bd590f543aad002a87acfd39de87ee33051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.5 KB (635482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c933a1486054ad16e8584e46e38e2ef1e897e6fc4fa3f66f9b4b97de5271d8`

```dockerfile
```

-	Layers:
	-	`sha256:6b5e189c5aa78dd5fddccfc95bf234149a022393a2645bd177315f8ffe24bdc5`  
		Last Modified: Sun, 19 Apr 2026 00:08:44 GMT  
		Size: 594.4 KB (594378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8628876e8e0fa6eea3a1ade6c2abba7c8804675d0f01fc31c1eeb017ec245d83`  
		Last Modified: Sun, 19 Apr 2026 00:08:43 GMT  
		Size: 41.1 KB (41104 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:18a48423ad812826df24af1bb144334e064b059a22725e59ef34c7ae9025467d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119355458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f1fb92dec3be5f5cc2f6e1680c1b712acc37a8377da0a2aa01b3ff09227137`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:03 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 17 Apr 2026 00:32:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Apr 2026 00:32:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Apr 2026 00:32:07 GMT
ENV LANG=en_US.utf8
# Fri, 17 Apr 2026 00:32:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 00:32:07 GMT
ENV PG_MAJOR=17
# Fri, 17 Apr 2026 00:32:07 GMT
ENV PG_VERSION=17.9
# Fri, 17 Apr 2026 00:32:07 GMT
ENV PG_SHA256=3b9a62538a8da151e807a3ddb1198e8605f2032544d78f403ae883d27ecf1ee4
# Fri, 17 Apr 2026 00:32:07 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:26:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:26:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:26:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:26:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Apr 2026 23:26:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 21 Apr 2026 23:26:14 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 21 Apr 2026 23:26:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:26:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:26:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:26:14 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:26:14 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:26:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b16b5e74609982c1b9aa44c4a27109093c4a3ba6b88e0e3fc5d1210eed2a213`  
		Last Modified: Fri, 17 Apr 2026 00:37:05 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1b45c8d73f888134c6fdd2bcde4cf95a1878d8360dcd10f1aa2c3e7fdead26`  
		Last Modified: Fri, 17 Apr 2026 00:37:05 GMT  
		Size: 894.2 KB (894238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320b21e60320ebeb63441338623b5d5915316e75a3824a868dfca204896c432f`  
		Last Modified: Fri, 17 Apr 2026 00:37:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd1e36dc43c56d1dc2b91e7600f5ffba62eb5cbc09b84770a72141ce5c0a3fd`  
		Last Modified: Tue, 21 Apr 2026 23:26:44 GMT  
		Size: 114.8 MB (114789729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10abfcd563c676f80b7f8d591833697648a314c3194234bf8913d746793efbc`  
		Last Modified: Tue, 21 Apr 2026 23:26:41 GMT  
		Size: 10.0 KB (9951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386fc68edbae25e1ef2d1913affe4d0755e86394896dd73cadad60bb2a46b445`  
		Last Modified: Tue, 21 Apr 2026 23:26:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd6d6b07825fda5a1a77d488174cbea427f579f0691d742eb7b237cf811fe3d`  
		Last Modified: Tue, 21 Apr 2026 23:26:41 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5fc1d9eb960373444ca2f6cb46f9da3a8f8f6b6d734b7ec8785bd2473a462e`  
		Last Modified: Tue, 21 Apr 2026 23:26:42 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdd42936b0a2ddc572b1ba47b2abedad1edae8adb2e21b36a1e7797619d92a0`  
		Last Modified: Tue, 21 Apr 2026 23:26:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:c212179503e5fc4a83e3b7dd1c7b84f9e408c0c3958ade43eb5ed59152429c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.4 KB (635418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10c5234ab28a69f0e090f0245b1af353529449b70624fbc6356696d5bbb9fb6`

```dockerfile
```

-	Layers:
	-	`sha256:b1a45fc22ddb467cd417007c11e405186219060aa31be33b326ed427a4fff287`  
		Last Modified: Tue, 21 Apr 2026 23:26:41 GMT  
		Size: 594.4 KB (594360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2762957ffd695c53f7bcb97e8780a3c1e395a3670b182294d2cc0818e99932d0`  
		Last Modified: Tue, 21 Apr 2026 23:26:41 GMT  
		Size: 41.1 KB (41058 bytes)  
		MIME: application/vnd.in-toto+json
