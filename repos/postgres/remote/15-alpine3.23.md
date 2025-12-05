## `postgres:15-alpine3.23`

```console
$ docker pull postgres@sha256:f395141c4fccd97672b54bde7a316b74a27eb34ead28b0e0b9e73bdaa88c01e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `postgres:15-alpine3.23` - linux; amd64

```console
$ docker pull postgres@sha256:59f8f5b36deb0139084fd85f15cdadf640ec24d0fba8b4ef78960d037088b8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109125241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ec7f558038145d32f0401ace3ae0a0d47cc67ec6fc0e25042027bd42c7c85a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:23:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 04 Dec 2025 22:23:15 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 22:23:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 22:23:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 04 Dec 2025 22:23:15 GMT
ENV LANG=en_US.utf8
# Thu, 04 Dec 2025 22:23:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Dec 2025 22:23:15 GMT
ENV PG_MAJOR=15
# Thu, 04 Dec 2025 22:23:15 GMT
ENV PG_VERSION=15.15
# Thu, 04 Dec 2025 22:23:15 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Thu, 04 Dec 2025 22:23:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 04 Dec 2025 22:25:12 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 04 Dec 2025 22:25:12 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Dec 2025 22:25:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 04 Dec 2025 22:25:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Dec 2025 22:25:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 04 Dec 2025 22:25:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Dec 2025 22:25:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:25:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Dec 2025 22:25:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:25:12 GMT
STOPSIGNAL SIGINT
# Thu, 04 Dec 2025 22:25:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Dec 2025 22:25:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607ed9a3591c5bdb3bbfeac29e54028e4e0491605b78f41c1cd8b49ab4218c34`  
		Last Modified: Thu, 04 Dec 2025 22:25:36 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccd5b0655f9266d126e171020167b40c0dfca221ae3f6dfceaf2b5cc4a4e6c5`  
		Last Modified: Thu, 04 Dec 2025 22:25:36 GMT  
		Size: 922.9 KB (922931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e9f761e408d49bc70d7fa839e87c7888a6520a7a0d722ef27ac913b887df8b`  
		Last Modified: Thu, 04 Dec 2025 22:25:36 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d376af2446a7d9d176deb032a4e5a0dbcd4eb34e036bfd52a7a2282914efbc`  
		Last Modified: Thu, 04 Dec 2025 22:25:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687c0957c6c4e3ce8d7f7bf00d5965e4de66a3eccbbf016097766ef76c27b815`  
		Last Modified: Thu, 04 Dec 2025 22:25:44 GMT  
		Size: 104.3 MB (104325986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237c2411b1e98b4495b3418463a4f1f6f6e0ad1b2bc7905708d5649ea780d235`  
		Last Modified: Thu, 04 Dec 2025 22:25:36 GMT  
		Size: 9.4 KB (9443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db59423165ded6cf9667203c52766a38098d0c4b748b47ce45942a3454264007`  
		Last Modified: Thu, 04 Dec 2025 22:25:40 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac52aa2f227dafb86793e17afbdb83632e47acf6ab6645aba4ad3181b9c550bb`  
		Last Modified: Thu, 04 Dec 2025 22:25:36 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136ae6a3f9741cfa08c84d7faee7da39a4fe43984886389554daf80482a58d2a`  
		Last Modified: Thu, 04 Dec 2025 22:25:36 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5b86e5dd6689ef8a1779cdb3758a650365bfed1cb74280c002146a59b217ac`  
		Last Modified: Thu, 04 Dec 2025 22:25:36 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:8bac496999887a3bf9802ac1b2e03782e73c17e56a4f0d94a0925e7bffe4960c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.5 KB (642470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab531019591c777714159af119eb5b1dce8e2053e0be916a582bd2b22455c0db`

```dockerfile
```

-	Layers:
	-	`sha256:273a8ffc8189c236dd42aa43416bce9b5bf427b0ba72f92f403f32c5f1e646ba`  
		Last Modified: Fri, 05 Dec 2025 00:08:34 GMT  
		Size: 598.1 KB (598080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16175729d58d47096a6608bc753b341c901219d97dd98e54b9e9a99a4849837d`  
		Last Modified: Fri, 05 Dec 2025 00:08:35 GMT  
		Size: 44.4 KB (44390 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; arm variant v6

```console
$ docker pull postgres@sha256:785176fd070f49bef8e897d4ec007e3e81dbd78266757589ad5612fb4875a86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88619947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e5fa6ecccbb53b01e81896f9a00a5f772d91166f3603d938abc416100c52c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:23:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 04 Dec 2025 22:23:47 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 22:23:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 22:23:47 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 04 Dec 2025 22:23:47 GMT
ENV LANG=en_US.utf8
# Thu, 04 Dec 2025 22:23:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Dec 2025 22:23:47 GMT
ENV PG_MAJOR=15
# Thu, 04 Dec 2025 22:23:47 GMT
ENV PG_VERSION=15.15
# Thu, 04 Dec 2025 22:23:47 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Thu, 04 Dec 2025 22:23:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 04 Dec 2025 22:26:38 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 04 Dec 2025 22:26:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Dec 2025 22:26:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 04 Dec 2025 22:26:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Dec 2025 22:26:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 04 Dec 2025 22:26:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Dec 2025 22:26:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:26:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Dec 2025 22:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:26:39 GMT
STOPSIGNAL SIGINT
# Thu, 04 Dec 2025 22:26:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Dec 2025 22:26:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8886bd73e9a0935281ab907f888d956eca4ece1d2863140df536ee8b1961e6d2`  
		Last Modified: Thu, 04 Dec 2025 22:26:58 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c635ab830074226abb1454caea254b577652ba8202a4d2eaa028b07f10ac90ba`  
		Last Modified: Thu, 04 Dec 2025 22:26:58 GMT  
		Size: 889.5 KB (889465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6984ee863a61f057d81550e160f256187436b7a5208391138e879d565ba429a7`  
		Last Modified: Thu, 04 Dec 2025 22:26:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42804e1aa7328373546339c12de9e19ad9426dce24bc60f0fbfbbf52793bf1d`  
		Last Modified: Thu, 04 Dec 2025 22:26:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49cb50a3d1a256677eddcc9b826ff7a4cb35e0bb2a7f8a587c46c8a6d8dd4d3`  
		Last Modified: Thu, 04 Dec 2025 22:27:06 GMT  
		Size: 84.1 MB (84145561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc99134be24f72d9d242389754a25a0ec895eef7855c02f6eed427f54a4bf54f`  
		Last Modified: Thu, 04 Dec 2025 22:26:59 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24cbb51e6e731d1ade7f3616d9fa58802cc80e44971600208c9e5f5c03912bc`  
		Last Modified: Thu, 04 Dec 2025 22:26:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444094f13535f36d874738e69d59f9bf33888546a55bfa72be51e4e4ec43dac6`  
		Last Modified: Thu, 04 Dec 2025 22:26:59 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ee1e2cfd59c68754e4ad9bf156c3be59630a258dc6afc5fefc9a0b02f2f454`  
		Last Modified: Thu, 04 Dec 2025 22:26:59 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77676014164386d4339024e363e4ceae5b3d17b67d9b8618240201c0c463162a`  
		Last Modified: Thu, 04 Dec 2025 22:26:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:d08a73e56f5c0e1bffef196f002e0a6931bf82431e1841cad0ef2710d2ffa5b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 KB (44353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfb370a39622b7347dae800f53beb5c6bc1a79a34fd2b45941d522d9b4f2633`

```dockerfile
```

-	Layers:
	-	`sha256:3de7901be43060238d6bcb1d7a0f81230854f208f16dba66a20d62b7abfa69af`  
		Last Modified: Fri, 05 Dec 2025 00:08:38 GMT  
		Size: 44.4 KB (44353 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; arm variant v7

```console
$ docker pull postgres@sha256:00ec3094d83dd548bb3ec20150bdf29950c0d402fa99e8b2309b2f8788b2527e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83872129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f65182ccbc631c2d0d293978a9b0199332b89cfb40a4700a3c5f8ff664c1364`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:20:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 04 Dec 2025 22:20:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 22:20:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 22:20:40 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 04 Dec 2025 22:20:40 GMT
ENV LANG=en_US.utf8
# Thu, 04 Dec 2025 22:20:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Dec 2025 22:20:40 GMT
ENV PG_MAJOR=15
# Thu, 04 Dec 2025 22:20:40 GMT
ENV PG_VERSION=15.15
# Thu, 04 Dec 2025 22:20:40 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Thu, 04 Dec 2025 22:20:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 04 Dec 2025 22:23:26 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 04 Dec 2025 22:23:26 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Dec 2025 22:23:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 04 Dec 2025 22:23:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Dec 2025 22:23:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 04 Dec 2025 22:23:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Dec 2025 22:23:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:23:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Dec 2025 22:23:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:23:26 GMT
STOPSIGNAL SIGINT
# Thu, 04 Dec 2025 22:23:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Dec 2025 22:23:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5d2a7d518cb5b185ddf7ec5e83a377b7b77575bb029575fb41aa67b510581f`  
		Last Modified: Thu, 04 Dec 2025 22:23:45 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c266160c31856dca6ddd6a708eaca3a421c207a9c4d8d83bf9899c27042b5cc4`  
		Last Modified: Thu, 04 Dec 2025 22:23:45 GMT  
		Size: 889.5 KB (889481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff3cddbec353d444054a3ddc7ad588abc68b590887a0d097f470134833b0a2f`  
		Last Modified: Thu, 04 Dec 2025 22:23:45 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d816390ab60e31ccac172640e7fb539c6a0ac6c243d82bee461636ab096385`  
		Last Modified: Thu, 04 Dec 2025 22:23:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329c060df2551e814259b1efb563b2e03eb8ca88802ca632d0bf289d217ccd7f`  
		Last Modified: Thu, 04 Dec 2025 22:23:54 GMT  
		Size: 79.7 MB (79687158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e7c23975c47d3731a5ad70e66837fbf872448cb96e3c9fec95a139b9f8ce09`  
		Last Modified: Thu, 04 Dec 2025 22:23:45 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9618bd891ddcc6980f87101ac7195c0b761332b5d259bba3ed074cb5b1c9e57a`  
		Last Modified: Thu, 04 Dec 2025 22:23:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84aed96cbbd2de2e51017cdc96a0f381883392322315f4ed01d1661df959eb1`  
		Last Modified: Thu, 04 Dec 2025 22:23:46 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340cd2305a9e2871ce4f84a1497bd0c1b0093fdd42370f5eae94e10d4e2e9197`  
		Last Modified: Thu, 04 Dec 2025 22:23:46 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b17771d9362b6a5f289417c0a0514a458aecb694ced08a82c897ddab1d5b9f1`  
		Last Modified: Thu, 04 Dec 2025 22:23:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:07c32e149113024ee76e4fc7bb2de8e83512c45ee7360ed367262efd7e31c263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.0 KB (642034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531f87b5db5138776f81f960aaaecb011c089e946901496636af9f90f514d959`

```dockerfile
```

-	Layers:
	-	`sha256:1c332f842bb9dcd2753ebb7c2889f0ceeddd6f2a07e715fa837ff40f77b4e10e`  
		Last Modified: Fri, 05 Dec 2025 00:08:42 GMT  
		Size: 597.5 KB (597466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:533353a2b383be1c240cadc2bca63368ed908f8c027e3de3812d56d25b4a0390`  
		Last Modified: Fri, 05 Dec 2025 00:08:42 GMT  
		Size: 44.6 KB (44568 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:fb03c0351916babccc23efa02fdf295eeccd4fcb833e422a904fa1836945fa4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107324843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8d8fd859fbf2abcf55eb92566e7b8be71d623f65c28a85923d98e1262f9d89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:22:10 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 04 Dec 2025 22:22:13 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 22:22:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 22:22:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 04 Dec 2025 22:22:13 GMT
ENV LANG=en_US.utf8
# Thu, 04 Dec 2025 22:22:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Dec 2025 22:22:13 GMT
ENV PG_MAJOR=15
# Thu, 04 Dec 2025 22:22:13 GMT
ENV PG_VERSION=15.15
# Thu, 04 Dec 2025 22:22:13 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Thu, 04 Dec 2025 22:22:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 04 Dec 2025 22:24:23 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 04 Dec 2025 22:24:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Dec 2025 22:24:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 04 Dec 2025 22:24:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Dec 2025 22:24:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 04 Dec 2025 22:24:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Dec 2025 22:24:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:24:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Dec 2025 22:24:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:24:24 GMT
STOPSIGNAL SIGINT
# Thu, 04 Dec 2025 22:24:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Dec 2025 22:24:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e97dc1e9523a2e2b95d2d9bff9a6a783b5fb4a1e74411c97df9458af0bec49e`  
		Last Modified: Thu, 04 Dec 2025 22:24:50 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c81517b2ba21b03e56f0cf4228742aa7755279efe34d67aed80eae2828e349`  
		Last Modified: Thu, 04 Dec 2025 22:24:50 GMT  
		Size: 876.5 KB (876494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568ed5c55f5ac0af923d5f028f57b13efc56927c08789865a27117516dc16254`  
		Last Modified: Thu, 04 Dec 2025 22:24:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dbd340671c280cb180f714e99ad9f0617c67839131c2c079d4b53ec3f0d826`  
		Last Modified: Thu, 04 Dec 2025 22:24:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60a75448d3a1e00ce9024c108d427f141b228a0f646abbb6420a72001ade9da`  
		Last Modified: Thu, 04 Dec 2025 22:25:00 GMT  
		Size: 102.2 MB (102236128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7333eb9469fae4c07b99a0e62c271daad991f6d65468b5fe586257087d291061`  
		Last Modified: Thu, 04 Dec 2025 22:24:50 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff8a9c65954424db6d774aebfe015a929ebb1de0019fa2ce6f116dd3f1cfa99`  
		Last Modified: Thu, 04 Dec 2025 22:24:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16aeff8a60a608571140e12fe4e0395b79779c89a7bd0571f69123c3ee44f5ce`  
		Last Modified: Thu, 04 Dec 2025 22:24:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f719d4d3973fde767ec7752ac148ec08b86e32fe300d689488b5652ff5d4baf7`  
		Last Modified: Thu, 04 Dec 2025 22:24:50 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1575803360c13cc5d5406faf347564b692cccf177b4350670e159d3b69ad3ce`  
		Last Modified: Thu, 04 Dec 2025 22:24:49 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:e2686d49465efa2afa7fd6f8387d13b513c4cb2bbdf95f2762b949604a5a8465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.1 KB (642100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4396b19ef5728264aa6cd2de32362e624541a7d5556c818e45d69b8ca196a2d5`

```dockerfile
```

-	Layers:
	-	`sha256:99d67f9088e013128233d3160f942da6a447bb79ddba97d0c486b732455ef698`  
		Last Modified: Fri, 05 Dec 2025 00:08:46 GMT  
		Size: 597.5 KB (597486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2bdbc82ed18be074fd9bbb6b2c2f01cf8a6ebabb055a7d2531457230a17873`  
		Last Modified: Fri, 05 Dec 2025 00:08:47 GMT  
		Size: 44.6 KB (44614 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; 386

```console
$ docker pull postgres@sha256:22f3a9cf3d6f149b32bbf7a10fd5d7c3a2281a0904be73b572152d921944fc94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115188275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da46a045dc8ee2398f09b6ba57f298a948be3c041589791feff9633abcb4e7c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:21:18 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 04 Dec 2025 22:21:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 22:21:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 22:21:21 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 04 Dec 2025 22:21:21 GMT
ENV LANG=en_US.utf8
# Thu, 04 Dec 2025 22:21:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Dec 2025 22:21:22 GMT
ENV PG_MAJOR=15
# Thu, 04 Dec 2025 22:21:22 GMT
ENV PG_VERSION=15.15
# Thu, 04 Dec 2025 22:21:22 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Thu, 04 Dec 2025 22:21:22 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 04 Dec 2025 22:23:35 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 04 Dec 2025 22:23:36 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Dec 2025 22:23:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 04 Dec 2025 22:23:36 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Dec 2025 22:23:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 04 Dec 2025 22:23:36 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Dec 2025 22:23:36 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:23:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Dec 2025 22:23:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:23:36 GMT
STOPSIGNAL SIGINT
# Thu, 04 Dec 2025 22:23:36 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Dec 2025 22:23:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814bd3cee87c29749ead028fe7c20456d469a0e81af048d6654fc85027988d47`  
		Last Modified: Thu, 04 Dec 2025 22:24:02 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76c2839cead8ceb5a25c2a43e7b4d743ee1f6b45dee84153178e8dd2412fb2d`  
		Last Modified: Thu, 04 Dec 2025 22:24:02 GMT  
		Size: 893.2 KB (893250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8c16e3b2fb1800a101ec5eee32212b8f7f7d1612c6d4a56833124ebd682633`  
		Last Modified: Thu, 04 Dec 2025 22:24:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a1651c7d12ef06dc455ab28df8235442485a0a6e46ec58e279a15288ff4d9f`  
		Last Modified: Thu, 04 Dec 2025 22:24:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f3e6753c6e991c77410261715ee46a2b5027eab7afbd5f2a48ed2f600265fa`  
		Last Modified: Thu, 04 Dec 2025 22:24:13 GMT  
		Size: 110.6 MB (110592150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022e02ce90daf3e3287299a6bd94ae92079b061b792ce08949b0b10f0ca80665`  
		Last Modified: Thu, 04 Dec 2025 22:24:02 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81103cbdb3bb786c32e60cb0812731520461481aa40133b70cb52d646c13756`  
		Last Modified: Thu, 04 Dec 2025 22:24:02 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce8abe9b72fdba46318a318b66b933bffd435864af5950175e294128011b741`  
		Last Modified: Thu, 04 Dec 2025 22:24:02 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c3f30b115efa7263324d3116c7b2510d7014c427ced450bfba5fac071a03a1`  
		Last Modified: Thu, 04 Dec 2025 22:24:02 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b1d156b0158fcaea363c2cc93917ceef5a42f3a2dc66eb7658f64634b6b30`  
		Last Modified: Thu, 04 Dec 2025 22:24:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:f8d99a4bbea255cb6241e2378c2e380e969d6140e29243f75b9000e1581cbdc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.4 KB (642397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3962f570c459070dd7a1c7eb1b5900cca3680027fb07c041e2a3a93e4a1615`

```dockerfile
```

-	Layers:
	-	`sha256:a8bf31df5985543138075efa4c5b907ba366ad05583df5b0b404f7b62981678b`  
		Last Modified: Fri, 05 Dec 2025 00:08:50 GMT  
		Size: 598.1 KB (598055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2b0352ec848718736d349752d213f0d49ee33f7c61684d8e82eeab34dec0fd0`  
		Last Modified: Fri, 05 Dec 2025 00:08:51 GMT  
		Size: 44.3 KB (44342 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; ppc64le

```console
$ docker pull postgres@sha256:d1ab42d242c819ee2aace855d65d0fc52b1ec07be37ed34d17820d1dc0f76554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94018826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f90d4ed517a5c3265072b84cb7b399d2732f5aa49af5fa1a55cfaab8cdcee95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:19:51 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 04 Dec 2025 22:19:55 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 22:19:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 22:23:45 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 04 Dec 2025 22:23:45 GMT
ENV LANG=en_US.utf8
# Thu, 04 Dec 2025 22:23:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Dec 2025 22:23:45 GMT
ENV PG_MAJOR=15
# Thu, 04 Dec 2025 22:23:45 GMT
ENV PG_VERSION=15.15
# Thu, 04 Dec 2025 22:23:45 GMT
ENV PG_SHA256=5753aaeb8b09cbf61016f78aa69bf5cbdf01b43263f010cbf168c82896213aaa
# Thu, 04 Dec 2025 22:23:45 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 04 Dec 2025 22:29:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 04 Dec 2025 22:29:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Dec 2025 22:29:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 04 Dec 2025 22:29:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Dec 2025 22:29:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 04 Dec 2025 22:29:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Dec 2025 22:29:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:29:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Dec 2025 22:29:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:29:26 GMT
STOPSIGNAL SIGINT
# Thu, 04 Dec 2025 22:29:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Dec 2025 22:29:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4059a2642ea065ae9757b9cd6c221d9b0d807a288fbb5b3b03be28c3b5aa9d`  
		Last Modified: Thu, 04 Dec 2025 22:23:28 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d41ce6ede149d659ddaa70993ce94ba64657c097825ad22629ef91006c39d3`  
		Last Modified: Thu, 04 Dec 2025 22:23:28 GMT  
		Size: 881.5 KB (881510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3d91d986c7523cd10ce286064919887eb5e796181edfec89d476bed3fb3775`  
		Last Modified: Thu, 04 Dec 2025 22:27:38 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f995db5aeb16bb674933fc79864e619721c4e735d6ba5255f63850b3b63226d`  
		Last Modified: Thu, 04 Dec 2025 22:27:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaf251af9ad85ca24cb7c721d4969bf629c7d36e0f55a1d99087d73bbc594da`  
		Last Modified: Thu, 04 Dec 2025 22:30:18 GMT  
		Size: 89.3 MB (89293268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f608f48dbd7e35a1676ca08e1bc53221c9429a02054aeb8dbb124a20052a41f`  
		Last Modified: Thu, 04 Dec 2025 22:30:08 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f34e6f56c65f90f8420c48907e103c001f5a953b8841355b45159cc236e65c`  
		Last Modified: Thu, 04 Dec 2025 22:30:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4563ce50c8cb03ded4e612a457c3cee762ff3b8ec535063b331b7cdb699fab14`  
		Last Modified: Thu, 04 Dec 2025 22:30:08 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98321bf1627255183c2c61fe104df9b4eed4ede7cbf20ea440f8e7f22a2b1637`  
		Last Modified: Thu, 04 Dec 2025 22:30:08 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511d98458c095994b8193306bd90c6e92b6d39a4c1d8920ff353bdd004c5b2e4`  
		Last Modified: Thu, 04 Dec 2025 22:30:08 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:5a6ed211639f77fded0ac2b905dfc1411d5584eb087920afbdba57a07043b719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49851243d218202a762359aad2162739fccc136e641c9bbd7f9dc0e61a70f38b`

```dockerfile
```

-	Layers:
	-	`sha256:adbd819e6aabf51a2534665612282c0fbc9162c81e7f17744ef8043eaa68b200`  
		Last Modified: Fri, 05 Dec 2025 00:08:54 GMT  
		Size: 595.8 KB (595801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7979543a3dadb8e9dda69a83db2f1c899031ad965e51dc9c646dfd8697222d24`  
		Last Modified: Fri, 05 Dec 2025 00:08:55 GMT  
		Size: 44.4 KB (44442 bytes)  
		MIME: application/vnd.in-toto+json
