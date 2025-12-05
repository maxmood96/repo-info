## `postgres:16-alpine3.23`

```console
$ docker pull postgres@sha256:a5074487380d4e686036ce61ed6f2d363939ae9a0c40123d1a9e3bb3a5f344b4
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

### `postgres:16-alpine3.23` - linux; amd64

```console
$ docker pull postgres@sha256:1cfff9db9fcc42b6b7b40fa89f7e21c6bee36a1f4e37bfa171b8e76b02cc9f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109957385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f87503b2fe5ad2e0d209b1a55830db42eb3ecd3eaf1b583accb0091ab30bff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:23:11 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 04 Dec 2025 22:23:13 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 22:23:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 22:23:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 04 Dec 2025 22:23:13 GMT
ENV LANG=en_US.utf8
# Thu, 04 Dec 2025 22:23:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Dec 2025 22:23:14 GMT
ENV PG_MAJOR=16
# Thu, 04 Dec 2025 22:23:14 GMT
ENV PG_VERSION=16.11
# Thu, 04 Dec 2025 22:23:14 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Thu, 04 Dec 2025 22:23:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 04 Dec 2025 22:25:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 04 Dec 2025 22:25:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Dec 2025 22:25:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 04 Dec 2025 22:25:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Dec 2025 22:25:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 04 Dec 2025 22:25:30 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Dec 2025 22:25:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:25:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Dec 2025 22:25:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:25:30 GMT
STOPSIGNAL SIGINT
# Thu, 04 Dec 2025 22:25:30 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Dec 2025 22:25:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f6f59522f45c0bbef5042355835e10726b93e75b9825166f324a97c492fcff`  
		Last Modified: Thu, 04 Dec 2025 22:25:57 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e78465396baf0b1656d2e378f2e89d50f98675a016a81b712c5feceffc6ba88`  
		Last Modified: Thu, 04 Dec 2025 22:25:57 GMT  
		Size: 922.9 KB (922921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b924e33a5c158a4bd7c0ee75939b96f5cd57b63182b03a8aa369525845f81b9`  
		Last Modified: Thu, 04 Dec 2025 22:25:57 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b299441641bd70b8dab8c3f9504262e1dd4e4966e5932479f7edffe72884fc4`  
		Last Modified: Thu, 04 Dec 2025 22:25:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55a8fe65af64236547f5efee37c9b13d6be788d617bbb0da5246706168c3032`  
		Last Modified: Thu, 04 Dec 2025 22:26:07 GMT  
		Size: 105.2 MB (105158014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f8607ad35947dc7cae0160c861104831f4c649eb35980389ddb05b998001cc`  
		Last Modified: Thu, 04 Dec 2025 22:25:57 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55ea1610abd46521fafb38fdb1041081134f36866d309a0b7649706a4bfc0aa`  
		Last Modified: Thu, 04 Dec 2025 22:25:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a5df93b4fd57162a880de4321416c96416d6fa5f7416741de6193d64f076dc`  
		Last Modified: Thu, 04 Dec 2025 22:25:57 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ddc7a97eab5666e383a2c566430386e2787beac4518f1a7c8bff266e4fe841`  
		Last Modified: Thu, 04 Dec 2025 22:25:57 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9e3e4c9f2025a532bba10ac93277d7949bec32a7c766e5b788a6654ff50236`  
		Last Modified: Thu, 04 Dec 2025 22:25:58 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:dc371c712705a92ac0e5442f69833cc1176b9517f3b9ab50428e68350188b682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.4 KB (642386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4bf2a98f5fb4b746b3b26f65bdcb4d90639454ddd4595253efae6212d510299`

```dockerfile
```

-	Layers:
	-	`sha256:209aac2bf18ac43ad1272288d06b66a046f3258d38e7a29a6ef16359b2513867`  
		Last Modified: Fri, 05 Dec 2025 00:09:28 GMT  
		Size: 598.1 KB (598080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acae222801f3465fcd064bf3403b398205f9bc34c3ae6b2fae92539e2becf748`  
		Last Modified: Fri, 05 Dec 2025 00:09:28 GMT  
		Size: 44.3 KB (44306 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; arm variant v6

```console
$ docker pull postgres@sha256:594327ef9b46bf0ca7fd544d8160b13dd55aad2ec92538aaf2f53746a192d269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89373080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07981f2fd99a11d665dd7c420476b0074ff23fb0aae1fce22b67d4964940ec8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:23:29 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 04 Dec 2025 22:23:32 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 22:23:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 22:23:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 04 Dec 2025 22:23:32 GMT
ENV LANG=en_US.utf8
# Thu, 04 Dec 2025 22:23:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Dec 2025 22:23:32 GMT
ENV PG_MAJOR=16
# Thu, 04 Dec 2025 22:23:32 GMT
ENV PG_VERSION=16.11
# Thu, 04 Dec 2025 22:23:32 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Thu, 04 Dec 2025 22:23:32 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 04 Dec 2025 22:26:26 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 04 Dec 2025 22:26:27 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Dec 2025 22:26:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 04 Dec 2025 22:26:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Dec 2025 22:26:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 04 Dec 2025 22:26:27 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Dec 2025 22:26:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:26:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Dec 2025 22:26:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:26:27 GMT
STOPSIGNAL SIGINT
# Thu, 04 Dec 2025 22:26:27 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Dec 2025 22:26:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd0a0fe1cf69c95ec377bf571336e07d91a694d8c04355fb0770a49ac7f509e`  
		Last Modified: Thu, 04 Dec 2025 22:26:46 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e992d0927df4e34e50f96cd7ddf2ca4907d6ed36c1bde9d83aadd6a86822902f`  
		Last Modified: Thu, 04 Dec 2025 22:26:46 GMT  
		Size: 889.5 KB (889463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76730b282d257061145ddbc0479330936f2d8fdd40a083171fc728ff0dddc98d`  
		Last Modified: Thu, 04 Dec 2025 22:26:46 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb7e5c6e16a1bcbda8c8e36019d005a95f0dc133b4e7427e37102d9bdc5eb2e`  
		Last Modified: Thu, 04 Dec 2025 22:26:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf15deb2415fa17076232defa2294fa46c34ddd57aa1caa78206edc31f7abc5`  
		Last Modified: Thu, 04 Dec 2025 22:27:01 GMT  
		Size: 84.9 MB (84898590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50dc0ec8d2b04d4ce07c7a529ee7103b8be1c29edb6281de84b4675e736e594`  
		Last Modified: Thu, 04 Dec 2025 22:26:46 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6dc5f1ecdd8b30af58e142213f2e5d8eab3171d0ac76125bebed94533784e5`  
		Last Modified: Thu, 04 Dec 2025 22:26:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8dfbc48d91669425fd85e3e6199aacb6793a847ac42141d688c8ae65d95413`  
		Last Modified: Thu, 04 Dec 2025 22:26:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f219958c7b685f3d170564df916c1d046c9d55a81aca0418fd49dd7a532efd75`  
		Last Modified: Thu, 04 Dec 2025 22:26:48 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862cc26ef5e7fb43b96d38a65b861dbae0ba4ac8ea1cda9313f23835ce7482d7`  
		Last Modified: Thu, 04 Dec 2025 22:26:46 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:406e4f94e7da4a9db05ee02db13b4e9aa017ba46a99ffcd0677a137a000a8721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 KB (44269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf5d0885e84c9c96b3a7bf3aaebb8838de075818d5fd8ef6ea0bc623f497103`

```dockerfile
```

-	Layers:
	-	`sha256:475b15fabfe324499cf7f37675bf5ea9748ce5cec10408e5416ee710976c0e94`  
		Last Modified: Fri, 05 Dec 2025 00:09:31 GMT  
		Size: 44.3 KB (44269 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; arm variant v7

```console
$ docker pull postgres@sha256:34e8c81708fe712cbd005db34b0acef238f8d76a7d10a7b1885e36ff7b09ccfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84608497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4c6e2a5aaff02f5c0fecfcfdff066f9bd5904fd109a49293bfb54c75bc571d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:20:25 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 04 Dec 2025 22:20:28 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 22:20:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 22:20:28 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 04 Dec 2025 22:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 04 Dec 2025 22:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Dec 2025 22:20:28 GMT
ENV PG_MAJOR=16
# Thu, 04 Dec 2025 22:20:28 GMT
ENV PG_VERSION=16.11
# Thu, 04 Dec 2025 22:20:28 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Thu, 04 Dec 2025 22:20:28 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 04 Dec 2025 22:23:23 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 04 Dec 2025 22:23:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Dec 2025 22:23:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 04 Dec 2025 22:23:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Dec 2025 22:23:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 04 Dec 2025 22:23:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Dec 2025 22:23:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:23:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Dec 2025 22:23:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:23:23 GMT
STOPSIGNAL SIGINT
# Thu, 04 Dec 2025 22:23:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Dec 2025 22:23:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f390c8e62ac2d1194796b54c1967c2afbc60b505ac546b4d5659c77a3c8fd9`  
		Last Modified: Thu, 04 Dec 2025 22:23:37 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af2f96b6f8222e0e4462046fca9db26815afa3dd91a9eb8a1feeadd07a85ab7`  
		Last Modified: Thu, 04 Dec 2025 22:23:37 GMT  
		Size: 889.5 KB (889478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557a5beb061a85fe57e49375e77e4c7e8a3e8d2f7956ba609144d003f408df7f`  
		Last Modified: Thu, 04 Dec 2025 22:23:44 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afef7380777c6cb1277b9c1099903291e97389467b2750611c46d85b7f0d100`  
		Last Modified: Thu, 04 Dec 2025 22:23:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7fe2cc0e41710c9ea41874780b7562e62848fcaccafcca2d396cea0dd3b1df`  
		Last Modified: Thu, 04 Dec 2025 22:23:53 GMT  
		Size: 80.4 MB (80423427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1710bda12a7096ce12c7cbee824203cf4684d9c0d92cd977251a65caa76e16`  
		Last Modified: Thu, 04 Dec 2025 22:23:44 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9a8d186c2f35970fbc02b29feb99767889c9c470756724b9636523bb4a518b`  
		Last Modified: Thu, 04 Dec 2025 22:23:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9175681326ce1a5c65c13e125cb1a71289a1381d4862638b8b7438cf1b16e92`  
		Last Modified: Thu, 04 Dec 2025 22:23:44 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a263879164a37dae21ba931679c4a8d1bbdcd0764b1c54149fc12999c4ba07`  
		Last Modified: Thu, 04 Dec 2025 22:23:44 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4bec11eb767c358e70438bcca260f63062374da4a12e5d9e8c6b6a0d22c93d`  
		Last Modified: Thu, 04 Dec 2025 22:23:44 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:e11e345e05204c310bf8c7f4a7fa3b9efa965c089f74ae1005cdccd4cfd4e016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.9 KB (641947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6014b597e151420fba64e572efb02e90d9f3989383a8339b5e29a62f6294407b`

```dockerfile
```

-	Layers:
	-	`sha256:d25891d7554101382ab187c7536464763def58571e95eadb3b4379154d745a26`  
		Last Modified: Fri, 05 Dec 2025 00:09:35 GMT  
		Size: 597.5 KB (597466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5f35fc353efa684dabfe1d6e795ae20722fb4c1001db5a1852db29ced8bce55`  
		Last Modified: Fri, 05 Dec 2025 00:09:35 GMT  
		Size: 44.5 KB (44481 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:84849713d049d899d21fe207a529626d30f38ecc5f5f77376b172a16e3f5eae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108125700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ec082eae29dc4359267b70b70d1e62a987906214f882a8b4c93641a6e6a112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:22:29 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 04 Dec 2025 22:22:32 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 22:22:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 22:22:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 04 Dec 2025 22:22:32 GMT
ENV LANG=en_US.utf8
# Thu, 04 Dec 2025 22:22:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Dec 2025 22:22:32 GMT
ENV PG_MAJOR=16
# Thu, 04 Dec 2025 22:22:32 GMT
ENV PG_VERSION=16.11
# Thu, 04 Dec 2025 22:22:32 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Thu, 04 Dec 2025 22:22:32 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 04 Dec 2025 22:24:43 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 04 Dec 2025 22:24:43 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Dec 2025 22:24:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 04 Dec 2025 22:24:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Dec 2025 22:24:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 04 Dec 2025 22:24:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Dec 2025 22:24:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:24:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Dec 2025 22:24:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:24:43 GMT
STOPSIGNAL SIGINT
# Thu, 04 Dec 2025 22:24:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Dec 2025 22:24:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400bfd1ac53315cc4507f788a858506c58f48decfbecbfb1cf563d7de121ac4a`  
		Last Modified: Thu, 04 Dec 2025 22:25:08 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf685290faac939ac8948352e2d881e57af0bdea3ac420d74760c4ca389cac79`  
		Last Modified: Thu, 04 Dec 2025 22:25:08 GMT  
		Size: 876.5 KB (876491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a72d2ddbc6c629ecc6463efbd876128b7718fc82fcded8699ae02e173e8c26`  
		Last Modified: Thu, 04 Dec 2025 22:25:09 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e217854f4b346520bac3e9d946125a0c9973f10021410fbf56576183f386235b`  
		Last Modified: Thu, 04 Dec 2025 22:25:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f2f6661915810fb2589b1943db9aaad30caaf78ed97e9d5887473126b9efcc`  
		Last Modified: Thu, 04 Dec 2025 23:12:22 GMT  
		Size: 103.0 MB (103036881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd72bab03022113231c08e05030e6d240bc785aff633608fec3d25d2a02ef40b`  
		Last Modified: Thu, 04 Dec 2025 22:25:09 GMT  
		Size: 9.6 KB (9557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3db4eb53fcfc111a0159ec9be24d11350d3e74df0a9628db944ff95f194796a`  
		Last Modified: Thu, 04 Dec 2025 22:25:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47f1868d6bd7fb18d31a612f80a879f6282a67ca2711acf2eacc441df56859c`  
		Last Modified: Thu, 04 Dec 2025 22:25:09 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7003cd16136b9519c92f12b5e454d03280e08ac53dbc527774630e06fb4f02`  
		Last Modified: Thu, 04 Dec 2025 22:25:09 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ae1aa13ccc1ab5c346b2eb3a257fcd032d01e1579720a27546799a438379e7`  
		Last Modified: Thu, 04 Dec 2025 22:25:09 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:26983c3a5156016b585d73b0993f58b735bab15781514429a35b0e59e440e94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.0 KB (642016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761dbd3fe3fcfb94a45cf28e71483b5a8ba07c524202b6e710e0137086371f5d`

```dockerfile
```

-	Layers:
	-	`sha256:c78e72cd70a65a64bd4694ee694e5267094430bfd1dce17bd52c987dc95ea2a9`  
		Last Modified: Fri, 05 Dec 2025 00:09:39 GMT  
		Size: 597.5 KB (597486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ed08e274433c1afc440e8c4a3df5e8564fa18cb46996ac794c462ed3e056dc1`  
		Last Modified: Fri, 05 Dec 2025 00:09:39 GMT  
		Size: 44.5 KB (44530 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; 386

```console
$ docker pull postgres@sha256:a257e6abb1f28ba239368fc125a600fc2ae1b7979ebcb12d6cdd10577896ead8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115976991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffe19becb52fedc75d6325929ad8c803c751947ba6b95011aae88eb6311c9a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:21:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 04 Dec 2025 22:21:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 22:21:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 22:21:17 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 04 Dec 2025 22:21:17 GMT
ENV LANG=en_US.utf8
# Thu, 04 Dec 2025 22:21:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Dec 2025 22:21:17 GMT
ENV PG_MAJOR=16
# Thu, 04 Dec 2025 22:21:17 GMT
ENV PG_VERSION=16.11
# Thu, 04 Dec 2025 22:21:17 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Thu, 04 Dec 2025 22:21:17 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 04 Dec 2025 22:24:01 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 04 Dec 2025 22:24:01 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Dec 2025 22:24:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 04 Dec 2025 22:24:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Dec 2025 22:24:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 04 Dec 2025 22:24:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Dec 2025 22:24:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:24:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Dec 2025 22:24:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:24:02 GMT
STOPSIGNAL SIGINT
# Thu, 04 Dec 2025 22:24:02 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Dec 2025 22:24:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7999846fe919ed79c4873b1f6c0ff35255fdb90e38b79f6ae62484d22b0794e`  
		Last Modified: Thu, 04 Dec 2025 22:24:28 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3d676c71994e92e672dd7142bdd39777ffe0fb3f2abfeaa42e23ed965322f6`  
		Last Modified: Thu, 04 Dec 2025 22:24:28 GMT  
		Size: 893.2 KB (893246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1faee2e277296338d20d2fe8c2c5cf36567e51aafc2c68b8e0c75e769de4e756`  
		Last Modified: Thu, 04 Dec 2025 22:24:28 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c1087ea3dfbfb502c190652976ecd03b1929747b96620311a05c6efa740eec`  
		Last Modified: Thu, 04 Dec 2025 22:24:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7f201dce8f4f6e590b2b082066bc717dbfe408b33f31cc5aa171a092b45e91`  
		Last Modified: Thu, 04 Dec 2025 22:24:51 GMT  
		Size: 111.4 MB (111380759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea2e62d3181df12c1980810913e533d3bce6eebdb3c17105ed0c093f4c0b6ae`  
		Last Modified: Thu, 04 Dec 2025 22:24:28 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbec5473e1ee175998f3a569d4dcf6d2f568e92b4e6c56a312c2249021c1b70a`  
		Last Modified: Thu, 04 Dec 2025 22:24:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ec7dac5d058b48ed5e2addfef663f57530055c4017352a5076ddcf2d5e36fe`  
		Last Modified: Thu, 04 Dec 2025 22:24:28 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f3129d80a6ec8e19e5f49dc7bdc7201213a8fd2603cb1e6b0ee6b925bfe6e0`  
		Last Modified: Thu, 04 Dec 2025 22:24:29 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205e0ec8b6c41e7b2ebcfe75459844b72c274c6a5ec13e7e4f142f64b4a172b0`  
		Last Modified: Thu, 04 Dec 2025 22:24:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:ac8df8961124b5c6e7dffc19e82e53857a59bcb43bd44eab975f31f9667ae081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.3 KB (642313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6c33fc86dd4552748d07e3f19fab852c475f5e8070b442f170834299486ff1`

```dockerfile
```

-	Layers:
	-	`sha256:c2b2a899934919e19f5c28ae05c22cfc7fda6ea3a8b52de2cc0db39354edacbb`  
		Last Modified: Fri, 05 Dec 2025 00:09:43 GMT  
		Size: 598.1 KB (598055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49527118a87c5d54f1f79f348092fcdeae29a04a4ec6edc21df945d215f5aa48`  
		Last Modified: Fri, 05 Dec 2025 00:09:44 GMT  
		Size: 44.3 KB (44258 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; ppc64le

```console
$ docker pull postgres@sha256:89a3b92bb21b1ed31c93eb8b7502a24784b8331fde51c7f12dc4b171078cedd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94862528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed88a788a449a3848f2b392d33b8974bd729178afd43ea1e5d347b9d5145f5b`
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
ENV PG_MAJOR=16
# Thu, 04 Dec 2025 22:23:45 GMT
ENV PG_VERSION=16.11
# Thu, 04 Dec 2025 22:23:45 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Thu, 04 Dec 2025 22:23:45 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 04 Dec 2025 22:26:45 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 04 Dec 2025 22:26:48 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Dec 2025 22:26:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 04 Dec 2025 22:26:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Dec 2025 22:26:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 04 Dec 2025 22:26:56 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Dec 2025 22:26:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 22:26:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Dec 2025 22:26:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 22:26:57 GMT
STOPSIGNAL SIGINT
# Thu, 04 Dec 2025 22:26:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Dec 2025 22:26:57 GMT
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
	-	`sha256:d294ffc562995e7103109a796a31c162bf046839bde6e6ed7dc48dbcde3b96d6`  
		Last Modified: Thu, 04 Dec 2025 22:27:44 GMT  
		Size: 90.1 MB (90136852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869b514089fca17e9347b6c961b24094389bcff38ccf5c68bec19bafd295ed28`  
		Last Modified: Thu, 04 Dec 2025 22:27:38 GMT  
		Size: 9.6 KB (9567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f1d10f1add46859450ed7fd43fda82c111aa71d9e561c2d449fccda05ce93b`  
		Last Modified: Thu, 04 Dec 2025 22:27:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6dbc3f2964a66e54c68190ce75ea5aa16c60841017b5ad7900700e83af1b4d2`  
		Last Modified: Thu, 04 Dec 2025 22:27:38 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b115d13378278ef4f10a03d2ac3889ca5a275ce0be397ed20c7b1f63a607ad5e`  
		Last Modified: Thu, 04 Dec 2025 22:27:38 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6563059ad19cc56879166c883952930fc546024cff60a526b9e492ecfab4fa6b`  
		Last Modified: Thu, 04 Dec 2025 22:27:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:db3e3f4ad0edb4b42c119f5c91e3e9eefc49a79b37dca7939e6b3b5032f428a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082cf4ac18940463fac5284d8a9c7c07ecb262dc39f04e5e0e402c43fac1b282`

```dockerfile
```

-	Layers:
	-	`sha256:150f252d50971dd3492f495343df1687d4165a13efedcc6e397a7e63c2402071`  
		Last Modified: Fri, 05 Dec 2025 00:09:47 GMT  
		Size: 595.8 KB (595801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de9449d5c203d9048787b82cebf4b3dbdbcf1d6928d082f2659c8d7d27b43c0`  
		Last Modified: Fri, 05 Dec 2025 00:09:48 GMT  
		Size: 44.4 KB (44360 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; riscv64

```console
$ docker pull postgres@sha256:f9228cf84a000b999505edd4962447227e09eb92531220041096d714c025f567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (111001473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462f99de6ab59267a8771b0839cc48ece09ba1e96d298bb50ce8d59f24c2f294`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Fri, 05 Dec 2025 02:43:01 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Dec 2025 02:43:13 GMT
ENV GOSU_VERSION=1.19
# Fri, 05 Dec 2025 02:43:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Dec 2025 04:35:17 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 05 Dec 2025 04:35:17 GMT
ENV LANG=en_US.utf8
# Fri, 05 Dec 2025 04:35:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Dec 2025 04:35:17 GMT
ENV PG_MAJOR=16
# Fri, 05 Dec 2025 04:35:17 GMT
ENV PG_VERSION=16.11
# Fri, 05 Dec 2025 04:35:17 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Fri, 05 Dec 2025 04:35:17 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 05 Dec 2025 05:26:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 05 Dec 2025 05:26:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Dec 2025 05:26:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Dec 2025 05:26:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 05 Dec 2025 05:26:10 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 05 Dec 2025 05:26:10 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 05 Dec 2025 05:26:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Dec 2025 05:26:10 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Dec 2025 05:26:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Dec 2025 05:26:10 GMT
STOPSIGNAL SIGINT
# Fri, 05 Dec 2025 05:26:10 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Dec 2025 05:26:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291664bb8b7dce2743daba44876e9622d0c6ab2de65fb226fa5a2e612de439e5`  
		Last Modified: Fri, 05 Dec 2025 03:36:44 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d15cb3651c4771f5468271552714d25e62e20e17b4276e4586757bf9431562`  
		Last Modified: Fri, 05 Dec 2025 03:36:44 GMT  
		Size: 868.9 KB (868912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f78884ec967782a1f7641a86df1658a1653d4def626b68d47a02aa5a82fafdd`  
		Last Modified: Fri, 05 Dec 2025 05:29:25 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab38f3998be163f3cda2ea55d15f2f2c51f6628f69ef79a512c06edea32df402`  
		Last Modified: Fri, 05 Dec 2025 05:29:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7633163c0d0af9cabe813ed4fe898924976b17cf57b84e58f4eb32af5b7319d3`  
		Last Modified: Fri, 05 Dec 2025 05:29:33 GMT  
		Size: 106.5 MB (106531893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f4ecd0f7f41353d972e84bc65bb87d95a84a3ee31c4a4c4e6bc8676fd5443b`  
		Last Modified: Fri, 05 Dec 2025 05:29:25 GMT  
		Size: 9.6 KB (9565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac26f02fb334a9f2ea89aff1ade66746b1021867a670e2274daabf8a7f9c92a`  
		Last Modified: Fri, 05 Dec 2025 05:29:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759943318d106de2508bef3fd3778b705e34abbf7ccc0a6b053435329d36ed85`  
		Last Modified: Fri, 05 Dec 2025 05:29:25 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30295e30b041137c73a72743782f2ebae925f1ed443b073f61285cd7fcbc83d5`  
		Last Modified: Fri, 05 Dec 2025 05:29:25 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1a7e91e4112f7beca6a07af5f777f36f2e8705630dbbb26399ba348a880393`  
		Last Modified: Fri, 05 Dec 2025 05:29:25 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:1da2ce798016ab18a193309e1f1c9ae597b0b5b44d4468cacb19e92fd8681f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.8 KB (641825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37eb588ea8f517c8e9e10ef22e080e6e7b4fadca197aa99d40116792809c0a7`

```dockerfile
```

-	Layers:
	-	`sha256:f3ee23a13391a56c946baec5d96f24dc789bbded47cfb347e4f3291d5532124e`  
		Last Modified: Fri, 05 Dec 2025 12:08:25 GMT  
		Size: 597.5 KB (597459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c73cc268be51f0934f5ee9e7f61c91c60e836eff7009352f042c29a65a10e930`  
		Last Modified: Fri, 05 Dec 2025 12:08:26 GMT  
		Size: 44.4 KB (44366 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; s390x

```console
$ docker pull postgres@sha256:241ff2bca511e067fc3a3d5b9c3a4945d1d45136effb935da5a311d39c2af450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118078445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9c1f776daccc6779789920a37d9146fcba0f9b5501ca19e6d4b1bbdec46a17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 23:32:11 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 04 Dec 2025 23:32:15 GMT
ENV GOSU_VERSION=1.19
# Thu, 04 Dec 2025 23:32:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Dec 2025 23:32:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 04 Dec 2025 23:32:16 GMT
ENV LANG=en_US.utf8
# Thu, 04 Dec 2025 23:32:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Dec 2025 23:32:17 GMT
ENV PG_MAJOR=16
# Thu, 04 Dec 2025 23:32:17 GMT
ENV PG_VERSION=16.11
# Thu, 04 Dec 2025 23:32:17 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Thu, 04 Dec 2025 23:32:17 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 04 Dec 2025 23:38:54 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 04 Dec 2025 23:38:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Dec 2025 23:38:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 04 Dec 2025 23:38:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Dec 2025 23:38:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 04 Dec 2025 23:38:56 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Dec 2025 23:38:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 23:38:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Dec 2025 23:38:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 23:38:57 GMT
STOPSIGNAL SIGINT
# Thu, 04 Dec 2025 23:38:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Dec 2025 23:38:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31b9e3ed8f234d25da4738dca8de16b285b5a453ad26e857eb6742400fc5080`  
		Last Modified: Thu, 04 Dec 2025 23:39:44 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c834da8b996b863bb6aa0daa48ea611323d5cecc5362f9d668703a853b581d6`  
		Last Modified: Thu, 04 Dec 2025 23:39:44 GMT  
		Size: 897.4 KB (897395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55088b85eb8144810ea1845069800f19e81451e2fc22f16e7621edd9b907be1a`  
		Last Modified: Thu, 04 Dec 2025 23:39:49 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da173dca1e0f160d57c2146b8d8e7837adc1e59f3511773b5a395c588af68684`  
		Last Modified: Thu, 04 Dec 2025 23:39:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5548590b67f1df4416495a86288200ad001df04f5c2b1aacae1163962c0e9f12`  
		Last Modified: Thu, 04 Dec 2025 23:40:17 GMT  
		Size: 113.4 MB (113440100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842ff607621b6843db746d66915f583801f66cc90377204436a38312886d69da`  
		Last Modified: Thu, 04 Dec 2025 23:39:49 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e3f5ece87b85d128be8a39083e7f3457b946e0a6287d231844dcc524a1717c`  
		Last Modified: Thu, 04 Dec 2025 23:39:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db7d32f7f397bd4a38bb435f193d15fcad6a099616bbf6972cf992c0a1aafba`  
		Last Modified: Thu, 04 Dec 2025 23:39:49 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e627bd425f6f4fb7c5b6045c447c2a1cab3cb38f410b0d38170c2b30184194e9`  
		Last Modified: Thu, 04 Dec 2025 23:39:49 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98cbd89da7a807765430ca0789f9e01745d1f4837e824502fb90f1b0cbd1e5e`  
		Last Modified: Thu, 04 Dec 2025 23:39:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:27553c4f3f238a850f46e62253774d998e210e8fc4ff47020c4a049483a1d7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.7 KB (641735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fff74b2a8601dbbb8353f3dd312f6e8ed27d050bfb3002c85c7098474383599`

```dockerfile
```

-	Layers:
	-	`sha256:0cb66eb746c426becefea27de0c84eb92258d54fe54ae969780610cfce6b0bf9`  
		Last Modified: Fri, 05 Dec 2025 03:08:33 GMT  
		Size: 597.4 KB (597429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d4c1888a96dd67631dc4c14dd2ada6e4f0d9846b55a321de7915e395b60ac05`  
		Last Modified: Fri, 05 Dec 2025 03:08:33 GMT  
		Size: 44.3 KB (44306 bytes)  
		MIME: application/vnd.in-toto+json
