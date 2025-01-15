## `postgres:12-alpine3.20`

```console
$ docker pull postgres@sha256:be11061c020d4b9a117265233b79bb0c25c19ac8d7d1e831c021f2da3fbd14d5
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

### `postgres:12-alpine3.20` - linux; amd64

```console
$ docker pull postgres@sha256:6cfb2bc482073562be13af4ea748d1a6b5b6bfcab66d86f20af1dca9913c7ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93165463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2718c07028230bdbc0d21f365b86970ca401985c816dac4e902fc6a4e9d014`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=12
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=12.22
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=8df3c0474782589d3c6f374b5133b1bd14d168086edbc13c6e72e67dd4527a3b
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae28dba45de3b28ad0efb3c8713f5902ad9b1c2dfedde1e6993800a97c1c488`  
		Last Modified: Tue, 14 Jan 2025 23:19:43 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5df0018e42c34af310f1f484aecf8654d12fce8961ba4f71a3ae26d8a04dec0`  
		Last Modified: Wed, 15 Jan 2025 09:40:50 GMT  
		Size: 1.1 MB (1120286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfd1540e170cb9ea6b8e284649af12c623033694d9056d5d9a2683551ad93be`  
		Last Modified: Tue, 14 Jan 2025 23:19:44 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e2adfb58feb61d9946216c571c16e17507394ad0d1141337b7286e63d45b8f`  
		Last Modified: Tue, 14 Jan 2025 23:19:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2076949814281b2737004521888fec15e64a21e6de763127e0391ff37070b9`  
		Last Modified: Wed, 08 Jan 2025 18:15:05 GMT  
		Size: 88.4 MB (88403059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efffca0bd1b9c0a5305e724d2fc71a5727c3e959abdf6681a3eacc1869edee3`  
		Last Modified: Wed, 08 Jan 2025 18:15:02 GMT  
		Size: 8.7 KB (8685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd22cfad0fbdc09b5ae68d3e952a191b3a12521177ffd371d7898c32daf0be23`  
		Last Modified: Wed, 08 Jan 2025 18:15:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f881d11e78e06d005ee0cbae1399dde5183f375bb3f946f3e1ae48442274a35a`  
		Last Modified: Tue, 14 Jan 2025 23:19:51 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e85b9fec4e71d94d7a365230150e0e1acad563714e8d5465c5efca83887da2a`  
		Last Modified: Wed, 15 Jan 2025 09:40:56 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a874be561f26d391d5d20481a953bce906fc5938d673fb6f7629db39eed2278f`  
		Last Modified: Wed, 08 Jan 2025 18:15:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:eab61102a48ae3f442430fd453d86145e0d3399be2d47ca9082f1f33220d5524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.3 KB (631269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634d380db1f79da0e94d37ecdea3cf7bc43b3b6628287247d763adb627d5074c`

```dockerfile
```

-	Layers:
	-	`sha256:06627a01720b9b043cf99763c3b73a9608ec8b0cca5c286dae556792ecf7a79a`  
		Last Modified: Wed, 08 Jan 2025 18:15:01 GMT  
		Size: 586.6 KB (586581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f8ece4ccc80ba684a93a9e4753c50b92e66df6f0a86c2ef09ba00bdc0d5fa6`  
		Last Modified: Wed, 08 Jan 2025 18:15:01 GMT  
		Size: 44.7 KB (44688 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:da3b4601ecd67a34429541306bb2c60790133b0ecbd85fe84256ae3a51c83fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92050930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26c3a8b2cb4c3aa8620678c200bf565266af719d77ad62807aae9723fb6092e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=12
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=12.22
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=8df3c0474782589d3c6f374b5133b1bd14d168086edbc13c6e72e67dd4527a3b
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Tue, 14 Jan 2025 20:34:27 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88efc830b0008c442fbf41800df30ca9fb0c00964fddd3e80890961627c5b9b8`  
		Last Modified: Wed, 08 Jan 2025 21:05:18 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0135973424a59bcd09d82651ba32d24eda2b75299b4d2e3f5deba54f7b2553`  
		Last Modified: Wed, 08 Jan 2025 21:05:18 GMT  
		Size: 1.1 MB (1086512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4b0d2c7f42b79dc01dbd3833f6c268867a01749968770c19b0a257a02954cf`  
		Last Modified: Wed, 08 Jan 2025 21:13:33 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b35d591cbe9900f8759fa3be037a5061e3b63755c2fd7f4c9e8ae8112697b1`  
		Last Modified: Wed, 08 Jan 2025 21:13:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b57cbb3728d57332776d130f20d2d1a18223696a3e367f11443ad3c50cdb4d3`  
		Last Modified: Wed, 08 Jan 2025 21:44:24 GMT  
		Size: 87.6 MB (87577083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286e6fe7d0d115c50bdff52419801537dafd3689e60bf2b628f23ac60e8cee64`  
		Last Modified: Wed, 08 Jan 2025 21:44:21 GMT  
		Size: 8.7 KB (8686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606468c0912df8de156af1f51c7fde90798b582b21585fe71c4dca589a65bf0f`  
		Last Modified: Wed, 08 Jan 2025 21:44:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32445c0717c13b6238a191836a8fdabd498fafec8fdb3f88416829a00e1cf317`  
		Last Modified: Wed, 08 Jan 2025 21:44:21 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765d54fb330ce802f267cd270c304221e4d34ec48fccd19dbca8585383c909f2`  
		Last Modified: Wed, 08 Jan 2025 21:44:22 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2891dc7ab4bb4e3f17eff1217ed6a24ab71839b5251b99859c0a6c2c06e391`  
		Last Modified: Wed, 08 Jan 2025 21:44:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:9f122ae56d933ef9b0db8cce22e21a0ec3ca3d64179c923b3f316f589018e881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 KB (44636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e72af8c017b1895ffec75ac55fe5bbd58250814bbd13a23767d7f49ff5843b2`

```dockerfile
```

-	Layers:
	-	`sha256:c432ad58ae36979e3131dacb5121757a6dddb8dd16cf56b7eaf6452137c0e97c`  
		Last Modified: Wed, 08 Jan 2025 21:44:21 GMT  
		Size: 44.6 KB (44636 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:7eb9eae868ff6f380477158c7c5d3efb1b00889461a13747ccf0a3e956dcf1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86563103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b279d9e0b122534a66afc6edd1ce8b004ab3c7650d5ec51b7367541b7652640`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=12
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=12.22
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=8df3c0474782589d3c6f374b5133b1bd14d168086edbc13c6e72e67dd4527a3b
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Tue, 14 Jan 2025 20:45:20 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b746070b0d0b0e37202f22f09fce21559849b7cfc62d09b1ccc2c4d324ce4b88`  
		Last Modified: Wed, 08 Jan 2025 21:11:35 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af679bfaf56ffe9fecae43f4b7f02611bb9b4a9d9be36b50592229008b20fc0`  
		Last Modified: Wed, 08 Jan 2025 21:11:35 GMT  
		Size: 1.1 MB (1086516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a574428493c8bb9e03f453f358c30456195031ee6dc5fdbcd31eb4c12324e1dc`  
		Last Modified: Wed, 08 Jan 2025 21:19:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbe265cd4c437408918c4e836299d627a0ce5979cbf59cc33e9bab1e3dd6262`  
		Last Modified: Wed, 08 Jan 2025 21:19:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbc465c9ab7546e8c1086e3f13fde2078d730c8cbfb1c51cdc59e117219f32e`  
		Last Modified: Wed, 08 Jan 2025 21:49:56 GMT  
		Size: 82.4 MB (82365206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41b957cd3ce2761e00ddf096bcc85d433d231564d41cbb6e9b26502b0f79865`  
		Last Modified: Wed, 08 Jan 2025 21:49:53 GMT  
		Size: 8.7 KB (8688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d6decdbba9bb4a01d59fb865a20a7c5b9ec5bb8ace2ee9e1489d58dac5abdc`  
		Last Modified: Wed, 08 Jan 2025 21:49:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e154f8d8f92683e7100ade2d42307673f041545ecd53146a39722c8e8c52449`  
		Last Modified: Wed, 08 Jan 2025 21:49:53 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f7be588c18a917afd13a7c6969bb22d1d0b02da6207b57db90013bd11d50db`  
		Last Modified: Wed, 08 Jan 2025 21:49:58 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d596594f3932dab733678060b6d59b8e873831a282966e43274115072b708c2`  
		Last Modified: Wed, 08 Jan 2025 21:49:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:0e4e1b5154835b77f66223d3af192d7275c46b1e3aa0e92984ef68db71bf5ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.5 KB (631453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cff31d427a779cd8230e7b28e3a7dc875e3d6fec8bd085f49271acff2f1ffb7`

```dockerfile
```

-	Layers:
	-	`sha256:ec2bdbbf42f52644c0dc3a2d72377aaa0a3d14d75818fcfa4d75fefe6d6a41f3`  
		Last Modified: Wed, 08 Jan 2025 21:49:53 GMT  
		Size: 586.6 KB (586601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b7afbf1c41168628b7dc0577c341f4bd8ed33fb90c2f8310edbf7b85e6f3094`  
		Last Modified: Wed, 08 Jan 2025 21:49:53 GMT  
		Size: 44.9 KB (44852 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:61b2fd9998b6605bf4d6af2be1382e04bac08e19a2906b8251edd3c8e71ae093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92478422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b9b1eef6741aedbcf2ce1cd397dca86d4fddc90599fa41b817f0aec258df1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=12
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=12.22
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=8df3c0474782589d3c6f374b5133b1bd14d168086edbc13c6e72e67dd4527a3b
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d44399ea45a930603df43b60dc9b107535c6cf565758aadbb124b0eec4bee00`  
		Last Modified: Tue, 14 Jan 2025 21:58:35 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad7be62d19dbe32494df2ba4a737e440946b4a8373c47d5a600dba48ed6adab`  
		Last Modified: Wed, 08 Jan 2025 21:23:45 GMT  
		Size: 1.0 MB (1049757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25a5092df8e17dac09425f12b17a14dedd5d271ab884d779a0a9b5116c6f7d5`  
		Last Modified: Wed, 08 Jan 2025 21:29:35 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0ce2df9d0312a11aac7fa86527a4967d9ccf652813cfe5cac4d3d08b1d887f`  
		Last Modified: Wed, 08 Jan 2025 21:29:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412cdec89044f956f6a46529525cb9c0594f59bceaa3837fcf0141bccf995c51`  
		Last Modified: Wed, 08 Jan 2025 21:51:24 GMT  
		Size: 87.3 MB (87322032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b8da1b358b35ee7c6f38ffba2b4a5f2fc05f0685cf0acd47453582ff55080c`  
		Last Modified: Wed, 08 Jan 2025 21:51:22 GMT  
		Size: 8.7 KB (8687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09dda72054fb2e382ec79b1ca67016dac452149b512309ae07a5b81bc2169bc`  
		Last Modified: Wed, 08 Jan 2025 21:51:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7edc8b78dfb09ac7892f1ee311da88fffacfb41805b964c572c4a1ff252f29ec`  
		Last Modified: Wed, 08 Jan 2025 21:51:22 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e677f739e3836428752072aebfaf16d8d289a0e2e40fcc8b86fc1e2853669c`  
		Last Modified: Wed, 08 Jan 2025 21:51:22 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b49483780cde88dc7ed662410fc817a4ddae180ff2cdb736fcbafe5cd59f294`  
		Last Modified: Wed, 08 Jan 2025 21:51:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:0054fa56ddb6205057235b1116559b1070935af7582ea7f42875d48f57815340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.5 KB (631500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8585dd16b7e5515befc0b3dd37842987340ce9fc4b8bd5c2c41d314dba107d1`

```dockerfile
```

-	Layers:
	-	`sha256:ae3393563487e73a684aede783d60d3e33d106f304627496612739c263d92377`  
		Last Modified: Wed, 08 Jan 2025 21:51:22 GMT  
		Size: 586.6 KB (586613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b8f667c384be913ed96cde70c61293db9c7826863542f6943633dcd318f625`  
		Last Modified: Wed, 08 Jan 2025 21:51:22 GMT  
		Size: 44.9 KB (44887 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:c180385d99d8b4e3f9d99c92ea61952e9eddd1c338f4aef110ba2e6955be35d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98407003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be762fe62643f1f0f30cdf774c078e35b848e2eea5acc610112aa4e79414e5dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=12
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=12.22
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=8df3c0474782589d3c6f374b5133b1bd14d168086edbc13c6e72e67dd4527a3b
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659ce32caae4f57c0acfec9e83363e92f335ac1a0818caec7a385ab0ef76c91c`  
		Last Modified: Wed, 08 Jan 2025 18:10:31 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a678b9ac7ee01a82d38b79bf9fd00f03737ee97bb6d41e5a4441d88f2f5839c8`  
		Last Modified: Wed, 08 Jan 2025 18:10:31 GMT  
		Size: 1.1 MB (1095376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948c739137bd17ccbe8085ea0d5197dba8112a2adfe5641a4a8a183f13f10ed5`  
		Last Modified: Wed, 08 Jan 2025 18:10:31 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3431cabc32c1205e3ce63e299a4672273fc2cb88575e7efc171e41218f7192`  
		Last Modified: Wed, 08 Jan 2025 18:10:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858ecf7389253409f5a7f243e877a6636bf31e9d4ee8aa55102c3b5c2b2f14b4`  
		Last Modified: Wed, 08 Jan 2025 18:10:35 GMT  
		Size: 93.8 MB (93824801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636dbc193381bbe9a8f088bae91ff61fbef6020a09b6d196a13d895ae0b3f10d`  
		Last Modified: Wed, 08 Jan 2025 18:10:32 GMT  
		Size: 8.7 KB (8687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd589487afe64b277731a4d1c47aa6d089e0c1cfb19e6c09a476884d638d886e`  
		Last Modified: Wed, 08 Jan 2025 18:10:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4328126466ff2f85312b04f4a27bd8ba08dbbae189c17fbdc8c29d19f6f9bc`  
		Last Modified: Wed, 08 Jan 2025 18:10:32 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2210fa69fa574487101eb712482e1a26785be47356e948487ca9a8c64db36b0c`  
		Last Modified: Wed, 08 Jan 2025 18:10:32 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f78b3d5f0f92fd164e4d303fbe6328910d6ade97f89de8176d90d55c7c04a9d`  
		Last Modified: Wed, 08 Jan 2025 18:10:33 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:314c1bc9318292b7e0b1d2344776582f85f6acb35bd6df1b537a6f3906b7e0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.2 KB (631216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ef89c78dac52dcf8279fa923dd78a6021a8dc5f547420f9d952e8dfaf674b3`

```dockerfile
```

-	Layers:
	-	`sha256:0d0fe8a96b07f00d9eb2c4a729ca5f503b527d1d6b80721e34fb7ecb718e400b`  
		Last Modified: Wed, 08 Jan 2025 18:10:31 GMT  
		Size: 586.6 KB (586566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00e4edbfd485a0394406db3a4973f76cf177d3a16c4267d9c934d0b426fb5dfa`  
		Last Modified: Wed, 08 Jan 2025 18:10:31 GMT  
		Size: 44.6 KB (44650 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.20` - linux; ppc64le

```console
$ docker pull postgres@sha256:b57cabebc925fafd189e3dab9c835d139cbf941c14add84c11a7fb271cc40cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97566763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4648fa6252d212bfd65c2cad7411c22ab2d45bf5837c9fb1a04f3b7e12be1652`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=12
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=12.22
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=8df3c0474782589d3c6f374b5133b1bd14d168086edbc13c6e72e67dd4527a3b
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd99b41e4eab97b8e99f151e356a73dcfdc6852319a226acefd789ac0a0fcdf6`  
		Last Modified: Wed, 08 Jan 2025 20:47:42 GMT  
		Size: 987.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01865a7aee85aee7eba24c5081ddf5c11e292c121e446bf7b6b6e679c5942374`  
		Last Modified: Wed, 08 Jan 2025 20:47:42 GMT  
		Size: 1.0 MB (1040020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98e8a6ccc51b487067716d0bf747e8eb0136bc2b9de2616369fb010565bff1f`  
		Last Modified: Wed, 08 Jan 2025 20:54:43 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b122119b1a97526cadfe6c461352381002a72b1f72b568d10edb1e12f012fc`  
		Last Modified: Wed, 08 Jan 2025 20:54:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8de567b49e8f0c9a691db1e486d43f53104ec76ffe5c0f88d04e7bd2dd26a4`  
		Last Modified: Wed, 08 Jan 2025 21:22:15 GMT  
		Size: 92.9 MB (92936464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d7899e415a2e459032cf86379075771f0bd75ffb0c6c62e5a79b74931619d7`  
		Last Modified: Wed, 08 Jan 2025 21:22:12 GMT  
		Size: 8.7 KB (8691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d6ce84fd4ff5a05fcd960c82b9ef4db0dd169a71ba604ea2b0ea10d993495b`  
		Last Modified: Wed, 08 Jan 2025 21:22:12 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1e788793f157ac96579e6b43ffd53ef019b5dcec6aeae00df1bc4feab776b3`  
		Last Modified: Wed, 08 Jan 2025 21:22:12 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df44e498995ff526464061fe56da12cbbc69b5114e3f2c7b111093cf1a4a8eb4`  
		Last Modified: Wed, 08 Jan 2025 21:22:13 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8517f2d3af1cd75b91e4cf7f1341ab3a2ca94eba6547ddc9acf2f5617f96bc09`  
		Last Modified: Wed, 08 Jan 2025 21:22:13 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:b111cb441e76cb8be351155bef5e64644baebc189976638f5b086ab9a7373f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.7 KB (627726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1700ca14d3741b4e8eceae6217a34ce979a23f9f8d5b3d615a987e46c3bb1a36`

```dockerfile
```

-	Layers:
	-	`sha256:6e01097612f23f81da22411c75d41adae034754b08df44de7db7efc0b066c6b4`  
		Last Modified: Wed, 08 Jan 2025 21:22:12 GMT  
		Size: 583.0 KB (582990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cc90d278486fb6e935ae54874137510d4417ef85225f215ec0b737b1ff3fea`  
		Last Modified: Wed, 08 Jan 2025 21:22:11 GMT  
		Size: 44.7 KB (44736 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.20` - linux; riscv64

```console
$ docker pull postgres@sha256:1261089c8c40ce7b9660743027bef6c8aaecb7fa4715d0df95b63647a0f9e450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93326954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c96a6cf79a8d3fe0cd920b7c12fd6e0d9fc74fedb9b8a2b5899626defdbfcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=12
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=12.22
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=8df3c0474782589d3c6f374b5133b1bd14d168086edbc13c6e72e67dd4527a3b
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Wed, 08 Jan 2025 17:49:41 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc93498547eda47632be52e4f9de0f535264be6b5b13bd695df74d21a445ee4`  
		Last Modified: Fri, 10 Jan 2025 08:04:23 GMT  
		Size: 988.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4379025cfe409827e83762b8ddf18bccb050a044fa62c5ba40f88f35ee905545`  
		Last Modified: Fri, 10 Jan 2025 08:04:23 GMT  
		Size: 1.1 MB (1089578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef0186356e321fef013e99e866a37e8308d9f788f5c47123b149b521575eec0`  
		Last Modified: Fri, 10 Jan 2025 09:45:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24206bd7240c9a3da106ad9224c974a577cee2bb13977c8f2b4de67741d06e77`  
		Last Modified: Fri, 10 Jan 2025 09:45:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a615e712efa1a9206a20fcb48e8d64e738672575861639d61e21e366fa5f116`  
		Last Modified: Fri, 10 Jan 2025 15:33:06 GMT  
		Size: 88.8 MB (88849572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa571faab43a480c299aba02069e356d60f3959f5f7d14690f440ebd9649db40`  
		Last Modified: Fri, 10 Jan 2025 15:32:54 GMT  
		Size: 8.7 KB (8692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089e6a38d08577fd7f61b1852e2d296bbd56c0c56f57e0d7bc119bdcaf085d18`  
		Last Modified: Fri, 10 Jan 2025 15:32:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6cb996e2a1f3612c162543982bb18bfb5928fc6d13be818b6a3af5073789ee`  
		Last Modified: Fri, 10 Jan 2025 15:32:54 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead5d36db822af632de2d0522816f8bf806975cda0da0a09705cec6b9bc755a5`  
		Last Modified: Fri, 10 Jan 2025 15:32:55 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474918b6d4c27befd3c8d07e53583ba43628421d14352747102a67b5a235b53c`  
		Last Modified: Fri, 10 Jan 2025 15:32:55 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:7c948ce5ee4baa01580bda2272b81588811c9ad3577a63e8f989a4541ecb7441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.4 KB (629384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcecd8d5c5884bc5b688eff46eddc569cec1d784f5a991fa0c626699b39f71b2`

```dockerfile
```

-	Layers:
	-	`sha256:2c6561d6a0837951bc54979f27db6a118fb9752c5ee2d8b50810bbb81f33fd3e`  
		Last Modified: Fri, 10 Jan 2025 15:32:54 GMT  
		Size: 584.6 KB (584648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:332df1b45049e3a363f2f7ac359e0699a7d2fbf766c77f1c6176f1791f49a4f1`  
		Last Modified: Fri, 10 Jan 2025 15:32:54 GMT  
		Size: 44.7 KB (44736 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.20` - linux; s390x

```console
$ docker pull postgres@sha256:4d61e2b39bfee157f7cff94d1e153c66ab78e6f7b6f1463e82f536e98fa649fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101896705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cd45fd9018d51a90aed360a0a7084ba7f5e56e8b6bb0156a5e20a112b1019f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=12
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=12.22
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=8df3c0474782589d3c6f374b5133b1bd14d168086edbc13c6e72e67dd4527a3b
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Tue, 14 Jan 2025 21:25:41 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc2876242de6bd7252b9ba2b4d53f4eb9fbcecfa1d99a33799aac75fa77090`  
		Last Modified: Wed, 08 Jan 2025 21:22:54 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864521ac5f08c5acac350319254a85153aba704edfa918f1373f4d3379e84be2`  
		Last Modified: Wed, 08 Jan 2025 21:22:54 GMT  
		Size: 1.1 MB (1084151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af466fe88aee254e0f612f2229ea0019a6fa590b2b240af14f886dc47d9b4d82`  
		Last Modified: Wed, 08 Jan 2025 21:30:40 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51451cadd271577a382834a257c7920101534a8811c78d1f30f05e05575cbf25`  
		Last Modified: Wed, 08 Jan 2025 21:30:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8e1c0c895f078d1f1717bffc4adf53bd28e2f222a1714da85e90df59852751`  
		Last Modified: Wed, 08 Jan 2025 21:59:53 GMT  
		Size: 97.3 MB (97333371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80396b2b586626a1a87a22b20057cb7c380a7a6acf56455c63c52fee7a65b3c0`  
		Last Modified: Wed, 08 Jan 2025 21:59:51 GMT  
		Size: 8.7 KB (8686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712768d7f6dcc2098d82fb55cf7913eed9aec5ed90a7365eef30383e70ac7b01`  
		Last Modified: Wed, 08 Jan 2025 21:59:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39638f927353802a1fcc8b1e2e32428923e4f1c2df6592c3b1eec08565429f`  
		Last Modified: Wed, 08 Jan 2025 21:59:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bb36478c52ac43c2f7546b20bc40b705e8eb196ffbd625f72d8c7e4631fba7`  
		Last Modified: Wed, 08 Jan 2025 21:59:52 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aea9dfa2d0f63fbbd43c5e128ef28af9e83386269f655011077f61f3fdbbb2d`  
		Last Modified: Wed, 08 Jan 2025 21:59:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:ee87effd42705d46d76ace897824306a065ee452a54bc17f00723580e4f46c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.3 KB (629318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345661a54aeb37da948de5be5c0d7071328ab5d1483392fc4296f8cc3edb1800`

```dockerfile
```

-	Layers:
	-	`sha256:8654e176dc8a6144d3f6432e596b405e89650e003c078c2cd95d97b615a85801`  
		Last Modified: Wed, 08 Jan 2025 21:59:51 GMT  
		Size: 584.6 KB (584630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58311d8284bde4e193f789bbffde94b41b7a89ffe457168088c81f1671a626f4`  
		Last Modified: Wed, 08 Jan 2025 21:59:51 GMT  
		Size: 44.7 KB (44688 bytes)  
		MIME: application/vnd.in-toto+json
