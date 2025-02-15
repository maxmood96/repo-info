## `postgres:15-alpine3.20`

```console
$ docker pull postgres@sha256:2e214cc180fcc6b80b4eed9747b2c5af54f9696484f47650fe1b640bc3fc02ff
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

### `postgres:15-alpine3.20` - linux; amd64

```console
$ docker pull postgres@sha256:2222b0eed2f86bbb7f36d705a823d8150562be4fe883a47af2657fcbd753e5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96216486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c503b639f3c70656ba0728c48b81431cb86908b99d106210dfcab64c104cdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 18:31:47 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:31:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_MAJOR=15
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_VERSION=15.11
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_SHA256=5367e97e81e493301cc4aab049dfbc9b4913822985bc62379faab2a281cfbdf0
# Thu, 13 Feb 2025 18:31:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:31:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:31:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:31:47 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:31:47 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:31:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c63abc240b3b922d1ccd53628ab26e8c322635907b753ee9cd85910763a5b`  
		Last Modified: Fri, 14 Feb 2025 21:12:35 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921e40087b1cc0113d897124e5ced2f51331fbc26c7fb348e682b07f125a898f`  
		Last Modified: Fri, 14 Feb 2025 21:12:35 GMT  
		Size: 1.1 MB (1120290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddba0de0cfacb732be730ce834063e995a760ca7443f71e999553a4e9b4c04a2`  
		Last Modified: Fri, 14 Feb 2025 21:12:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d855f16fefae54eec45de2dd79eee03f69ec89e896b389dfb801edbc096ad3de`  
		Last Modified: Fri, 14 Feb 2025 21:08:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2a31f6244926c21369e4087555eecb999435e549d7d0d7d5c7484d638cb737`  
		Last Modified: Fri, 14 Feb 2025 21:12:43 GMT  
		Size: 91.5 MB (91452682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f87d84dba7c50659dfe51b2e44458d9f0723bf1fc52532daacbbc0e9c5397b`  
		Last Modified: Fri, 14 Feb 2025 21:12:36 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0b7f1ce2acb44da6c7ae028873533860a70a67b92d7cae06b1674417febf50`  
		Last Modified: Fri, 14 Feb 2025 21:12:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f41a55bfe8191db776f7d3b310a4406562175cd855cf8d6eb86a075ce30d45`  
		Last Modified: Fri, 14 Feb 2025 21:12:37 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df102c386ee289d4f2a593b573b11b1d78c3e2abedb3635b4cf6addbfaaf8e17`  
		Last Modified: Fri, 14 Feb 2025 21:12:37 GMT  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e20cea72618a3faea3824782780720d8d2797288a49d7019e64760caa003b4`  
		Last Modified: Fri, 14 Feb 2025 21:12:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:ca2f10abdf851727a65f8c18febd17f0c43e0c4a686f3ab25e68bb7f5c7f83c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.3 KB (634330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f826283d1efbb9052100d17572a72707be9a321276d6ac925f3450838a921402`

```dockerfile
```

-	Layers:
	-	`sha256:0a977b86c6e620fa045150c2c5fb1eec86031ecd339fcb3e58114984c8371dec`  
		Last Modified: Fri, 14 Feb 2025 21:08:17 GMT  
		Size: 589.5 KB (589526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b287c41d8723574a73c82de03617e4b8d67758fcf89f1aa279e5bc38518616e5`  
		Last Modified: Fri, 14 Feb 2025 21:08:17 GMT  
		Size: 44.8 KB (44804 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:5d57d2533f63c58621610b313c4b511b114d848a7f7d358ee3a0545b05b725c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94947794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4781260fecb159229abb55ad7f350f65e6238ffa41d3a5dc0db78685081911`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 18:31:47 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:31:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_MAJOR=15
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_VERSION=15.11
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_SHA256=5367e97e81e493301cc4aab049dfbc9b4913822985bc62379faab2a281cfbdf0
# Thu, 13 Feb 2025 18:31:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:31:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:31:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:31:47 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:31:47 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:31:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 19:26:24 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f562bdeccc677affba17117a3e71eed437842fbd24407b2ce425aa5819d3dab5`  
		Last Modified: Sat, 15 Feb 2025 00:09:21 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c15f54b7c7b9df1d9b4f973855ca80d075a47a5343b27c0f6e4ae7774389b5`  
		Last Modified: Sat, 15 Feb 2025 00:09:21 GMT  
		Size: 1.1 MB (1086525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d568e84a40aff368bdcb0f2c0209c899ecf6614f22d843f7855cc038d42ed61d`  
		Last Modified: Sat, 15 Feb 2025 00:09:21 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464e90337bafdf4dac44e92da85d96c873b18c4c579abd3dd0ee24ba0ae61dc9`  
		Last Modified: Sat, 15 Feb 2025 00:09:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea39fc9f41112f5e4908a35292d746e2bae941705a8aeb7afa4495de2919785`  
		Last Modified: Sat, 15 Feb 2025 00:10:33 GMT  
		Size: 90.5 MB (90472106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279d4f3ab15bde9b6e3cebc9c53c75bf82e3f1f88dea33c9b838137d7d01ebc0`  
		Last Modified: Sat, 15 Feb 2025 00:10:28 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2ba4b25aebeef61de95b73146e1f264cc3b695bc01abdf067af8af13d3cddb`  
		Last Modified: Sat, 15 Feb 2025 00:10:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b3943d93aa7be5e630a4256e845f899f310a276512aa64fb643f89aa788f47`  
		Last Modified: Sat, 15 Feb 2025 00:10:28 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1d25b5d09138882201cc952ecf98ac811faa660911bbbf6ce8f9d93d76b649`  
		Last Modified: Sat, 15 Feb 2025 00:10:29 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2d3462f038e3830fdb4ef0ebb2dc3907a0963ba9b233d7a616481dddcba2f6`  
		Last Modified: Sat, 15 Feb 2025 00:10:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:dd7c928eb6480dd55efafe8cfddf898c68cb561218603ea17a07c036f7c07b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 KB (44753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65148ef6361ecc633bb5cacaa66da9363bcf14479caf4f6efece521c3f2c28ce`

```dockerfile
```

-	Layers:
	-	`sha256:ecb642c26c9e0a111fde0dd448c94bd098997a6c9bab7fb43af7730c554c0017`  
		Last Modified: Sat, 15 Feb 2025 00:10:09 GMT  
		Size: 44.8 KB (44753 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:ba7d7f44a3308b509c32ed9ef7d688ba4e6ea25f72758aa61c83136bb4ebd0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89355511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5884174765eee46d9ca0253e2045c3a39d08b331d69c217718010a4b66533c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 18:31:47 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:31:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_MAJOR=15
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_VERSION=15.11
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_SHA256=5367e97e81e493301cc4aab049dfbc9b4913822985bc62379faab2a281cfbdf0
# Thu, 13 Feb 2025 18:31:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:31:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:31:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:31:47 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:31:47 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:31:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 14:35:10 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25896e659de9add0d4b908897850cbf64b7928b4104747d7d2f865d03c785b5e`  
		Last Modified: Sat, 15 Feb 2025 00:24:03 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f74483a18f569a1fa2c939344a028b1612c307bf93662a4fdaf02c3f961ae8e`  
		Last Modified: Sat, 15 Feb 2025 00:23:59 GMT  
		Size: 1.1 MB (1086514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eadf93718700a6ae0148ccbb835c2325930ee0d12ad9dac188ce36572109a18`  
		Last Modified: Sat, 15 Feb 2025 00:23:55 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b8c5e4ce7a3e3769bc68c603e910cda8c227d7c7644ade020fd071c0811efb`  
		Last Modified: Sat, 15 Feb 2025 00:23:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df94b347454676738531fec27eaf172d7b115765380517d31a83d31110148f5b`  
		Last Modified: Fri, 14 Feb 2025 21:29:55 GMT  
		Size: 85.2 MB (85156404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d633440559378cdbf879b978c506480636d933477d8631b0014af2064d7ff4f`  
		Last Modified: Fri, 14 Feb 2025 21:29:52 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2c29df8f34dc203ede3f9c5f3566a6ff71c46558ed4bba89cdbb6be10b0170`  
		Last Modified: Fri, 14 Feb 2025 21:29:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b50cc8edf41478796e12f4505784ef5d12e975f3c3aa0f71bd7d9e29a32dfb`  
		Last Modified: Fri, 14 Feb 2025 21:29:52 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3529b7196c8155643ae7d071da29e194171e4f2d753cbb2410be053f12b12d1`  
		Last Modified: Fri, 14 Feb 2025 21:29:53 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d28db6c30c69c4085f92b68b20de21f9968a6eef90e864bc19e438f72db5ac7`  
		Last Modified: Fri, 14 Feb 2025 21:29:53 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:57152b76ee055dd817a4d5cb2ad57162408c9e5beca7a13e4a966b1740e342c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.5 KB (634514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5622fe8db5252f343cbf6d8a7cf156c843c1191b4dc338eb594ff2bcd9a518e4`

```dockerfile
```

-	Layers:
	-	`sha256:5a9f53b2214efd7bcd81c6d915d671a6a9089ef204614e2c16e51613ed4eae35`  
		Last Modified: Sat, 15 Feb 2025 00:10:10 GMT  
		Size: 589.5 KB (589546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d22b65f890b4144c66f84a246844cf8b762f93edd489d55aa767ea1a1aa1b2e7`  
		Last Modified: Sat, 15 Feb 2025 00:10:11 GMT  
		Size: 45.0 KB (44968 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:07dabba5011e711e0c3f0ce709df4f448214e9979588104c78fe459b16883e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95455129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145feac78b32a18542dbd7fe7311b8007d557d2f35e1b50a7b74b8b2660cdb69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 18:31:47 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:31:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_MAJOR=15
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_VERSION=15.11
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_SHA256=5367e97e81e493301cc4aab049dfbc9b4913822985bc62379faab2a281cfbdf0
# Thu, 13 Feb 2025 18:31:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:31:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:31:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:31:47 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:31:47 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:31:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc8827c16e8ec088d48c0b753a38f9b70fa76626b8e70929dbb63cf84cc89b5`  
		Last Modified: Sat, 15 Feb 2025 00:22:17 GMT  
		Size: 979.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0907d060ed36b58b8341b1b05e996014c48ca9a918bb7414420e2e27fa4bc054`  
		Last Modified: Sat, 15 Feb 2025 00:22:10 GMT  
		Size: 1.0 MB (1049755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36da590e94d03388333c8f90ebc9ff573b76757ec31fc8b18a031f6350a39911`  
		Last Modified: Sat, 15 Feb 2025 00:22:00 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba3a5783239b116fcb925eef91e91369b4580402ff73a02ffd413615c3afcf0`  
		Last Modified: Sat, 15 Feb 2025 00:21:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7691d6a0479686883774425dd8188a935a7b2978fcb2aadb8687aa4bb87525a9`  
		Last Modified: Sat, 15 Feb 2025 00:24:31 GMT  
		Size: 90.3 MB (90297590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112a49da8e9cd7b9349c4f950e74cf7c08a95ac0fc0fa5f1eba30e111518a5b8`  
		Last Modified: Sat, 15 Feb 2025 00:24:26 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218aebe1861e31ac2f30ed4aaf82ecf1499e69ee7ae9b84437a2ad955b56c178`  
		Last Modified: Sat, 15 Feb 2025 00:24:27 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27934fa5b36bf96929ec8404960cda97fc048eb1a6da11d47fcc6559b054e5f6`  
		Last Modified: Sat, 15 Feb 2025 00:24:28 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4399982e2694f9a0cb72d58410644b28c87da8e861f5a60f8f3457f55b36106e`  
		Last Modified: Sat, 15 Feb 2025 00:24:29 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd0ec2989c34ef92b6fe8a49bdc3630ee2f8417fb4cbf1684633a022bcb723b`  
		Last Modified: Sat, 15 Feb 2025 00:24:29 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:7b59db9608f4e07842b81df9305e63e8d32dd7a4d7d2bf8d45164d933bc23156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.6 KB (634562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca86f23e126c3e425834073a2c3f9370a7dfae728e506b50e7ebef61ab2af0c`

```dockerfile
```

-	Layers:
	-	`sha256:0bfcc53a3e960e9b750f5db8d47b3c8f814d559cad42105ed3a2a025afb78277`  
		Last Modified: Sat, 15 Feb 2025 00:10:12 GMT  
		Size: 589.6 KB (589558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a4d0c64b9a759b9c57a8b234557325daa319cb191b1e9224f4a8cb8951fa331`  
		Last Modified: Sat, 15 Feb 2025 00:10:12 GMT  
		Size: 45.0 KB (45004 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:a317e6b1dd53d2a8c19f87a41f143b1e9aeb98c7d3b65dc6a4e43b87c3363b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101561885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50865e46b9002a440454e6573f7b22d7d4f7572f5171fadea921d2548245e289`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 18:31:47 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:31:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_MAJOR=15
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_VERSION=15.11
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_SHA256=5367e97e81e493301cc4aab049dfbc9b4913822985bc62379faab2a281cfbdf0
# Thu, 13 Feb 2025 18:31:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:31:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:31:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:31:47 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:31:47 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:31:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 14:36:27 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a698c50ca401253ee0a1571a20b50701f87d4ff2aba3a00e3911050b6e5fb9`  
		Last Modified: Fri, 14 Feb 2025 19:26:34 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58e9a3b0a25ecb012a9ef00dd9abd46a7fff8279e7446197b36696b07085c3d`  
		Last Modified: Fri, 14 Feb 2025 19:26:34 GMT  
		Size: 1.1 MB (1095378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94caf2386289bf840a71263ceb34251b027ef80b965f42375f746957af98144`  
		Last Modified: Fri, 14 Feb 2025 19:26:34 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778e5be8f5eed361e99120a2046991f0b51b572491bae9320564f38d1a641f1c`  
		Last Modified: Fri, 14 Feb 2025 19:26:34 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d828a3e2582aa1c95e998e509f68b24f1cff3863f02f49d0b41437f7dba24c`  
		Last Modified: Fri, 14 Feb 2025 19:26:37 GMT  
		Size: 97.0 MB (96978225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1badd9809aa02e31e201816f3b9b1fe3005620009925b6fa697fd7d660c0d78d`  
		Last Modified: Fri, 14 Feb 2025 19:26:35 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d8398716ab7a201b3a5a13e630cb2cefb86a346634347de34b76fe0814f42a`  
		Last Modified: Fri, 14 Feb 2025 19:26:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ad5a0efefeb824d8cb9f712c08a4d24ccd647426e0df990bf2908194f18607`  
		Last Modified: Fri, 14 Feb 2025 19:26:35 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b455ec39ff54ce841ba75c28aeb100a863c30dea143e96f7ec6b276e82ffd0e3`  
		Last Modified: Fri, 14 Feb 2025 19:26:36 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaebaa8ebbef53f1a2de6bfb3057185fa4af536d01309831e25f55f2acd4cb5`  
		Last Modified: Fri, 14 Feb 2025 19:26:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:44b0f2083d17e30530aa61369d7431ed391c0e3d4ec9ebe563cc536ccbdcfd64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.3 KB (634277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f325f55dd0cb8cf4c29fda0a7dbd9a77d7f87e4d3c1603fbae1055820b461f4`

```dockerfile
```

-	Layers:
	-	`sha256:c217b72d9c006b004e71ec57763c6a43fc94ffad88a872739a3cecd444ccd482`  
		Last Modified: Sat, 15 Feb 2025 00:10:14 GMT  
		Size: 589.5 KB (589511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e184b90fcb83271a924c00b7d30745817c6fba464b5b44518798e0a1f6a7110`  
		Last Modified: Sat, 15 Feb 2025 00:10:14 GMT  
		Size: 44.8 KB (44766 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; ppc64le

```console
$ docker pull postgres@sha256:ca838949604c500ae7372424c132988a9f7bbee2b8065ea380464a8c3d0093a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100789703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fad22ccd9fadcf3332c3263a18f3a02262c24658538489e117cc958d47e3e2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 18:31:47 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:31:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_MAJOR=15
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_VERSION=15.11
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_SHA256=5367e97e81e493301cc4aab049dfbc9b4913822985bc62379faab2a281cfbdf0
# Thu, 13 Feb 2025 18:31:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:31:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:31:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:31:47 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:31:47 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:31:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 14:35:49 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4560e6eaf6136fe9ed082dd565c5a37bb5ec3e433bd72a01116ae44bd04994e`  
		Last Modified: Sat, 15 Feb 2025 00:18:37 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a2d29dc8697219ebfcfe5e6e5c56b2549f8e69e4f3f0bdf9803dcbf630c294`  
		Last Modified: Sat, 15 Feb 2025 00:18:31 GMT  
		Size: 1.0 MB (1040018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db695e36d82284dfc46d1fed4f570d9a812b952a1abb41603b09ccb4565b2b1`  
		Last Modified: Sat, 15 Feb 2025 00:18:24 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120127792b9f26a99d1a9584a1747e461b88ea90bd0e37882e377a843cc7930d`  
		Last Modified: Sat, 15 Feb 2025 00:18:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fad79047e42236f1c6582eac79dcdbf9996803388c5b0589e405eba3de5128a`  
		Last Modified: Fri, 14 Feb 2025 21:31:28 GMT  
		Size: 96.2 MB (96157385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe8a6785344e6bf661df9b92e29630ceb9fbd84e45087a6ca6a2564d7726e70`  
		Last Modified: Fri, 14 Feb 2025 21:31:25 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6975fca77430353c4ff2dd904026dec87c084d48ede8d66806d34acd60781ada`  
		Last Modified: Fri, 14 Feb 2025 21:31:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f76f73c2f2367c44adb03df58a168dd2ae37c1401d03286e30fc298022d37c1`  
		Last Modified: Fri, 14 Feb 2025 21:31:25 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3666ecefbfe4b877b998bda34037277b994128076b4b3fbdaaf273d5c5962508`  
		Last Modified: Fri, 14 Feb 2025 21:31:26 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b5140ab5502b441cebacb572ba8ac4f9c18e37ef55ca22a24cec579d3cf04f`  
		Last Modified: Fri, 14 Feb 2025 21:31:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:9865cef344e964195945b73510b3fecb3456d8297663ff1d6ef150cdcb25ff9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.8 KB (630787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2499a02cb87456d42e2c553db13aab7aa387a433c5af1a03d57a7c3f91cb27cd`

```dockerfile
```

-	Layers:
	-	`sha256:6d84e30a57d22cafab5bc1279ef928b38aa73b6ec41af747bd1ee9a9380b0472`  
		Last Modified: Sat, 15 Feb 2025 00:10:15 GMT  
		Size: 585.9 KB (585935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33a0217fe9d7eaadba9250639b70a44e1ef6dce74af093b7d8e9a922bcec14da`  
		Last Modified: Sat, 15 Feb 2025 00:10:16 GMT  
		Size: 44.9 KB (44852 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; riscv64

```console
$ docker pull postgres@sha256:e8e6d11efc80ca7999c9464fe55692659b7ca8dc3318290b8ed4fb7d361fc27a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.7 MB (98714942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff77fb415ea0143144c2ab05dd031c315be9d0122098ac282fb1223d0273afc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:31:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_MAJOR=15
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_VERSION=15.11
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_SHA256=5367e97e81e493301cc4aab049dfbc9b4913822985bc62379faab2a281cfbdf0
# Thu, 13 Feb 2025 18:31:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:31:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:31:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:31:47 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:31:47 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:31:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Tue, 14 Jan 2025 20:50:16 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc93498547eda47632be52e4f9de0f535264be6b5b13bd695df74d21a445ee4`  
		Last Modified: Wed, 05 Feb 2025 08:29:23 GMT  
		Size: 988.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4379025cfe409827e83762b8ddf18bccb050a044fa62c5ba40f88f35ee905545`  
		Last Modified: Wed, 05 Feb 2025 13:31:04 GMT  
		Size: 1.1 MB (1089578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef0186356e321fef013e99e866a37e8308d9f788f5c47123b149b521575eec0`  
		Last Modified: Fri, 14 Feb 2025 09:07:20 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24206bd7240c9a3da106ad9224c974a577cee2bb13977c8f2b4de67741d06e77`  
		Last Modified: Wed, 05 Feb 2025 08:29:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316f19b3b555d70c5040a8cbe843f6a740b04dd07f0bf7e1a9f3b643f8003c8c`  
		Last Modified: Fri, 14 Feb 2025 09:07:27 GMT  
		Size: 94.2 MB (94236800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe83729713ed27415c2f7ef2d5a03d67af5ab838f4a0083f04bec6421379b11d`  
		Last Modified: Fri, 14 Feb 2025 09:07:29 GMT  
		Size: 9.5 KB (9458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f28c07e5b25df2f340edd6f92421fc3564cf49853369849a8e506a531648a52`  
		Last Modified: Fri, 14 Feb 2025 09:07:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d9f1f505d9fef953c238f42cb08cb5389fb1550b2c76da2e03794a1ff2f9c4`  
		Last Modified: Fri, 14 Feb 2025 09:07:30 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c361c6b773eb4b950021293a242684f48fe3c7a54b05adaf67c8692f4e1abd41`  
		Last Modified: Fri, 14 Feb 2025 09:07:30 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d29ddfcb950b80dc68a866d54ff7fe562db90e9c629a15e5a70894f2f142368`  
		Last Modified: Fri, 14 Feb 2025 09:07:30 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:3009abd9c366278ae3667848605a536dd3a0afb85a3a70813e94ce4548b6091f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.5 KB (633466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af9019f6806715a4d9495f0eb6f5f15314942317984e4cde558c4d459f152bd`

```dockerfile
```

-	Layers:
	-	`sha256:473704d7ff8fe5aed6fbd69439a95802029ad295966f67711ee6658060d22093`  
		Last Modified: Fri, 14 Feb 2025 06:08:44 GMT  
		Size: 588.6 KB (588614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7977e2ddc8b06610d10dcf4114f6fa61e7a77daef9e7a0b1c35af7ce6b3781bd`  
		Last Modified: Fri, 14 Feb 2025 06:08:44 GMT  
		Size: 44.9 KB (44852 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; s390x

```console
$ docker pull postgres@sha256:1c7e447d85f20f856ce854ff4218ad0338e8f7242be2b7ff070f9f20fcdac134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105148932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44239c09174f47184a4c6649185ea589030785147aaeaddf656ebe017bf1a9bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 18:31:47 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:31:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_MAJOR=15
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_VERSION=15.11
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PG_SHA256=5367e97e81e493301cc4aab049dfbc9b4913822985bc62379faab2a281cfbdf0
# Thu, 13 Feb 2025 18:31:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:31:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:31:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:31:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:31:47 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:31:47 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:31:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 14:36:22 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bd808fe0e001bd5a66a02c69406d4cdeb252f933c590cb4d320052ea3b3546`  
		Last Modified: Sat, 15 Feb 2025 00:16:42 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b626b09720dc73a31296f38e3ebe6c64e8a0f0170f1d84c424109e9cbbfb03`  
		Last Modified: Sat, 15 Feb 2025 00:16:35 GMT  
		Size: 1.1 MB (1084163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5bfd3e663523426c97298e108c7d05f57cc63e280ad958b0489b777f37f192`  
		Last Modified: Sat, 15 Feb 2025 00:16:29 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2ec1e1feb3ecea6aa9ce13b57efbf5c29523f7ac7d7955c245fbebb7d1741a`  
		Last Modified: Sat, 15 Feb 2025 00:16:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc109bc13134fec67281b51cc72c4845ad98c01d80fd65e7fc0629dbd65f87a`  
		Last Modified: Fri, 14 Feb 2025 21:53:37 GMT  
		Size: 100.6 MB (100584024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6ab2ba57e933cd9568c57d5012b3e57826069cd37574b8f8d7d4bb053d9f70`  
		Last Modified: Fri, 14 Feb 2025 21:53:34 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fa68a1738b12bafb1f02038fe994b9ab197fc037403bce51bdc154335992fc`  
		Last Modified: Fri, 14 Feb 2025 21:53:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6273c000967202560c4d626fd04361cb5840cdd9379a36c9faf2c418deed193`  
		Last Modified: Fri, 14 Feb 2025 21:53:34 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70877ae378f32565ff9c337b0d0d0a43985d33be8f919fc5f182eee099d350ae`  
		Last Modified: Fri, 14 Feb 2025 21:53:35 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0524f206b0465aeabdd8eb6021ee04ab2d3023e85816467d0f189cf3c4a2e6bb`  
		Last Modified: Fri, 14 Feb 2025 21:53:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:69c53bfbb8bdef456b5ea51a14d239a33bb02439bdda61dc70a99eb25fda0fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.4 KB (632385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3672ac2643662fc24d651a73ddd0b3ed215f46af3e7676041566035cc9b5a822`

```dockerfile
```

-	Layers:
	-	`sha256:611fe1cf2c43796a53786692ab64875571322fe6001b585851f4aff5723f3fa7`  
		Last Modified: Sat, 15 Feb 2025 00:10:18 GMT  
		Size: 587.6 KB (587575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa254be34de248c5e1bb58197dbcbedec989a132bcfbb567d87f36ac82b9975`  
		Last Modified: Sat, 15 Feb 2025 00:10:18 GMT  
		Size: 44.8 KB (44810 bytes)  
		MIME: application/vnd.in-toto+json
