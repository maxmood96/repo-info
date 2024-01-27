## `postgres:13-alpine3.19`

```console
$ docker pull postgres@sha256:8fd0b91362d350ccd16eec5c5e06ab65f18596e6d3a568fd5032ff0b5b82a12e
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
$ docker pull postgres@sha256:aa8033f09a0186ac7f86e9bde9707b8d2dd2c100b372826ee025bdb2facdb62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92669137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa474ec2334a1d8f319445b483238ddd0102023eef1a57632de62a955836249c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 22 Dec 2023 00:27:15 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=13
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=13.13
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=8af69c2599047a2ad246567d68ec4131aef116954d8c3e469e9789080b37a474
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 Dec 2023 00:27:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
STOPSIGNAL SIGINT
# Fri, 22 Dec 2023 00:27:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92deedc7522e6d8fc6a2f178dfb23f9542287f93e5895f7a38085917325969db`  
		Last Modified: Sat, 27 Jan 2024 00:57:10 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85de3e8ba1c7d37eee9fa5829b2efe329d121e74593a26045904fb3b930ebb8d`  
		Last Modified: Sat, 27 Jan 2024 00:57:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fd19fdb1bada28523048976e51211b7083854793dc9c5bc58cf37d0d420ead`  
		Last Modified: Sat, 27 Jan 2024 00:57:11 GMT  
		Size: 89.2 MB (89244101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220defc8170e1bb50910c51cfc2450e5b48363034b83ac66743ca926edd3aaec`  
		Last Modified: Sat, 27 Jan 2024 00:57:10 GMT  
		Size: 9.0 KB (9022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9ede412d6fcbc93381d30afdae25a8a1a63c4b001e337187b1d0de55cf322b`  
		Last Modified: Sat, 27 Jan 2024 00:57:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b0e120d028efb5185de1f0e7a4c9cc962fcc7dd86c50652655ede8364b1af2`  
		Last Modified: Sat, 27 Jan 2024 00:57:10 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1adc912acdefaa9809e3cccb5424eff2f25d6f1558338773737d8c49ee74c98`  
		Last Modified: Sat, 27 Jan 2024 00:57:11 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7135718e38dcf6a5c81ac9a75d11f188a04c80f4a95aa810205a7f4850c927e2`  
		Last Modified: Sat, 27 Jan 2024 00:57:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:c0f16fd1ed8f4155ca4c4333ca559cf62a79a3494cd5918ecd8bd4f71d3be8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.0 KB (842021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f246bc8ecf5c6107f2de21cac78579ee9e9dad16090d996d8e9e3e52a3702e3`

```dockerfile
```

-	Layers:
	-	`sha256:dc278d75b9a7e953e2f817db909106fd7f496f14c8d9015832529708fe0430e2`  
		Last Modified: Sat, 27 Jan 2024 00:57:10 GMT  
		Size: 804.8 KB (804767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a563dee37b45ded1fc3d1e93f07d72e4a95672fb6416d27972b6300beeda673`  
		Last Modified: Sat, 27 Jan 2024 00:57:10 GMT  
		Size: 37.3 KB (37254 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:856f5d610e71a8350e23b83ad0ccd64786e89a0b408d194fc7ef2f5ad88114a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91470697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a42a4f9dc2b42c6e54aa228f2e8a6fe56c4177c235608a1a792e6590c74ef5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=13
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=13.13
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=8af69c2599047a2ad246567d68ec4131aef116954d8c3e469e9789080b37a474
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 Dec 2023 00:27:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
STOPSIGNAL SIGINT
# Fri, 22 Dec 2023 00:27:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b8fa596712ea779c4cb87ad98b3ad730138e4b5d96f64ec23a93cc60393aee`  
		Last Modified: Sat, 06 Jan 2024 11:54:19 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c59b03b6f5155de1f45d96c0cd184b8faf805859e9ea5a1eb7bb6cf3d2c38d8`  
		Last Modified: Sat, 06 Jan 2024 11:54:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f978a04c7f2c411cb02c85f24e9ba29f27cf7e98ce3a951e39298dbd42f33a`  
		Last Modified: Sun, 07 Jan 2024 06:44:45 GMT  
		Size: 88.3 MB (88289248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb64422237b8c0874f16238db5fd1894df207641bd061ccbff7be2990c235d1d`  
		Last Modified: Sun, 07 Jan 2024 06:44:42 GMT  
		Size: 9.0 KB (9024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ec59b8ff9efb842d3bf9e746efe3df96a53c837be14596123497aac8002b2a`  
		Last Modified: Sun, 07 Jan 2024 06:44:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcb2a9ee265fb1b29c2b49769af6adb2d72f24b0b184570279db36f8015d79f`  
		Last Modified: Sun, 07 Jan 2024 06:44:42 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebef6edfb6e91be5a28b2c9a0593f24f583d0ecfee4a8004de20855bd073071`  
		Last Modified: Sun, 07 Jan 2024 06:44:43 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3c5226ed6797a1e59fe63b940e5bda247aca6910be53dbc88d11350e75e381`  
		Last Modified: Sun, 07 Jan 2024 06:44:43 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:9e9cc98cbd6a375eb59318decba6a64706f3a83ee1907ecc50d60aef064f31bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 KB (37021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f3daa8a5fa89b3fc7aa4f43ca57abac75da85fe289c8b33ac3d0f5590999ee`

```dockerfile
```

-	Layers:
	-	`sha256:086bfe7966a6b8296bfea0b3bdad8dfd1d843df3133a78e0c1178be3413dde2a`  
		Last Modified: Sun, 07 Jan 2024 06:44:42 GMT  
		Size: 37.0 KB (37021 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:33d1bbc7b316674866fbec60c956054ffce8f73c6963af526d3a8c7ca83e553d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (85989682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99222fd7e2ea513028dadf1ef4ebd0b62c90cbf3f0a889c22a64a7c4209dccd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 22 Dec 2023 00:27:15 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=13
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=13.13
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=8af69c2599047a2ad246567d68ec4131aef116954d8c3e469e9789080b37a474
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 Dec 2023 00:27:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
STOPSIGNAL SIGINT
# Fri, 22 Dec 2023 00:27:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf782f407230cde68ad1fe94a87a82f2ee6564456dbb2e632ed6b9985a758725`  
		Last Modified: Sat, 27 Jan 2024 16:43:20 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab3bf70fcb637ceab1ecc0f8ba4e3d999807b3d3f99729e8585e51cbf9a8b7f`  
		Last Modified: Sat, 27 Jan 2024 16:43:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f994882f190475eff111dbb097341acf9e1d9f724f346fd3bce68045eda28f8b`  
		Last Modified: Sat, 27 Jan 2024 17:50:05 GMT  
		Size: 83.1 MB (83054482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6bb9e1d49651d3fb89b524c1748bf15f80e2c5b089143a42ac7e8b18f8e30a`  
		Last Modified: Sat, 27 Jan 2024 17:50:03 GMT  
		Size: 9.0 KB (9022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597196d1d56707c351fe09538b952a1a80a2e7769154364bca3ebf4980219d6c`  
		Last Modified: Sat, 27 Jan 2024 17:50:03 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974b55118f4cd553fc7c8abaef76fd2d891e02caf2f943a75161e26847148aa9`  
		Last Modified: Sat, 27 Jan 2024 17:50:03 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6d278d56a6ec938fe7144d6f944289111c5e6dd55365fe863874ad69b5c4a3`  
		Last Modified: Sat, 27 Jan 2024 17:50:04 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25413c3422ab2dd1b4e1c454086414605857f404a6e9b8a0fdba5671f589c15c`  
		Last Modified: Sat, 27 Jan 2024 17:50:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:9b14e4e513ccd49af3114f1f2f413978f14786f32ac54049666d61b429c02c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.0 KB (842039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1291998433898943248e6c9618e4e07bd16efa5b15314298cb5f34e6a9aec4`

```dockerfile
```

-	Layers:
	-	`sha256:608b8ff6064b69123c35d01601adff14d1b04cca8831340e7264ce9b3b7c0ff4`  
		Last Modified: Sat, 27 Jan 2024 17:50:03 GMT  
		Size: 804.8 KB (804803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b57f73a648d8bb970f6f8fa67fc35c51a9169f1fe7a62dad9a85a5107051e8bb`  
		Last Modified: Sat, 27 Jan 2024 17:50:03 GMT  
		Size: 37.2 KB (37236 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:16a52446af9dbdad2865117b8bb454e167da258eddcf9a7dc0e1e5cc157c25b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91453453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f931535b674dfcc96954178d1b5f385bf086f10ce78d6ef50b2cbee6286e760`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=13
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=13.13
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=8af69c2599047a2ad246567d68ec4131aef116954d8c3e469e9789080b37a474
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 Dec 2023 00:27:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
STOPSIGNAL SIGINT
# Fri, 22 Dec 2023 00:27:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a13ecc88456148cc73b8941875af2463232293d6e48313a5d057f52f188e04`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01277bc8c6d336069acfe7e4b99842b4e64eb3c6b65bd1dd31d3a6a8a1d98b16`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21004c696c0abdacea5fe14ddb0ffb2c7092333f236a369b4b96dafc92ecbb83`  
		Last Modified: Wed, 13 Dec 2023 04:17:44 GMT  
		Size: 88.1 MB (88089349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e83698d331de3026e5ebada8873e9a671c7d7b635dcda7d9ec22de4567f093`  
		Last Modified: Wed, 13 Dec 2023 04:17:42 GMT  
		Size: 9.0 KB (9022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a806d33b2581b954b0604de6760161e8a7dbfac92f04d3b593c25296c0e94d50`  
		Last Modified: Wed, 13 Dec 2023 04:17:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b625e6b9cecfc94dac744bddb48e0577b5d8b3e3f13b202b038d730f151251`  
		Last Modified: Wed, 13 Dec 2023 04:17:42 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2682223f4761e04b34dc5931781b21e2d3c11644888ed5b7109a26e5fe73e0b6`  
		Last Modified: Fri, 05 Jan 2024 02:32:24 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ba3770ac7288509419c5a26313736aef72e5bd990b130257ccc1c18f3fa192`  
		Last Modified: Fri, 05 Jan 2024 02:32:24 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:852bb7482e5757988f7d0d702ec64021e412477f2259553c329e118bfbd6f5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.9 KB (841870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e0cc6d468b29351abd6d6df8fb8b904046c3bb589578533c068016070d2072`

```dockerfile
```

-	Layers:
	-	`sha256:ac443762cfb7bcfcc9b8001a06d579a335225b89ec872f9b577319339f3e9786`  
		Last Modified: Fri, 05 Jan 2024 02:32:25 GMT  
		Size: 804.8 KB (804772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:273acab02a3b689b8a857e5fc71555cc69d165e9d1ecfea1264ef041277d3c70`  
		Last Modified: Fri, 05 Jan 2024 02:32:24 GMT  
		Size: 37.1 KB (37098 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:5f8198bbb23baaefdd1d60d5bb16a5419bdf3c769a58ae3958383f9054be5101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97910470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9b6798437bcbc4f84c4536651413db2fcf6a94f43b29e27e84953c360897d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 22 Dec 2023 00:27:15 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=13
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=13.13
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=8af69c2599047a2ad246567d68ec4131aef116954d8c3e469e9789080b37a474
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 Dec 2023 00:27:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
STOPSIGNAL SIGINT
# Fri, 22 Dec 2023 00:27:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2133def43d4644982362d414316dd83e009c687351246641a998c4ad71337c4a`  
		Last Modified: Sat, 27 Jan 2024 01:58:24 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f448b522721952d7c0e99fe32360fef5e126f78264ef9641a3cb6b2fa727d693`  
		Last Modified: Sat, 27 Jan 2024 01:58:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01d125d5bdf789f1c561338434359221c73687e31d5f6ea5d551e7a4ec90dbc`  
		Last Modified: Sat, 27 Jan 2024 01:58:27 GMT  
		Size: 94.7 MB (94650082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf4eb655098c70954bb40f49105671066135574a3370381331ac86adc01e5ee`  
		Last Modified: Sat, 27 Jan 2024 01:58:24 GMT  
		Size: 9.0 KB (9020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239e8a25a350cb1786ee1eba3f0fa967ffafca93511987c2dfce07f28c7a5f0a`  
		Last Modified: Sat, 27 Jan 2024 01:58:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea47e9c5d52ae222604ec96b2fcce841e471082d9ff2454fc201091d2a8ea3ae`  
		Last Modified: Sat, 27 Jan 2024 01:58:25 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9c44e53609eb59859697279f4eaf0398197a3c824a3b088dab125836ba5434`  
		Last Modified: Sat, 27 Jan 2024 01:58:25 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b69793a4772f3a3dded8bc093eed062c12955879bdcc6e133e77827ff420be`  
		Last Modified: Sat, 27 Jan 2024 01:58:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:9d8506101d815d8f56b9b005bf2f26cd12004e32b41f37daa5a93ea7d0f230f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.0 KB (841955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9afa26649da4ff78b701b478b10817115db0171abd9015e6a30b245722ef36`

```dockerfile
```

-	Layers:
	-	`sha256:03c1c4cd669682b087fea83b2777b23bcac90e8c0d21bfbc7feed492d621b07d`  
		Last Modified: Sat, 27 Jan 2024 01:58:24 GMT  
		Size: 804.7 KB (804742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b66f8ac649c5ac537af58882840a71ad7d40d69d1f4afabd62d03604916141b`  
		Last Modified: Sat, 27 Jan 2024 01:58:24 GMT  
		Size: 37.2 KB (37213 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:e05e2604442d5c731d6c45e86882cc264e6e80a77148b225b3619fbf6f5ca604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97108433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062523174a0046b966d16d836c1ff4b0cdbc109813a495641c45b37bd2feeb54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 22 Dec 2023 00:27:15 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=13
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=13.13
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=8af69c2599047a2ad246567d68ec4131aef116954d8c3e469e9789080b37a474
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 Dec 2023 00:27:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
STOPSIGNAL SIGINT
# Fri, 22 Dec 2023 00:27:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2095ef6b4fb4fda18e7742c1ae925254b33c6a16e337ac453301de35138c9807`  
		Last Modified: Sat, 27 Jan 2024 10:14:06 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf89a242212848a6e54b111c1643243666bfac60a2cbca3b3fb15c09c6fcff78`  
		Last Modified: Sat, 27 Jan 2024 10:14:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10271fa7c78abdb4309bd212cf6007a79390e0eb8376e5c5e0f3f204f7f48d6d`  
		Last Modified: Sat, 27 Jan 2024 10:32:44 GMT  
		Size: 93.7 MB (93733777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fb0ce0a6402a34127a60929cca2cf75143aef62e1e7d31de4911976eaed942`  
		Last Modified: Sat, 27 Jan 2024 10:32:41 GMT  
		Size: 9.0 KB (9026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9984f510c1478065ff0afc4aef519d5492e22ca621f18d4bd5056c35b1fd908`  
		Last Modified: Sat, 27 Jan 2024 10:32:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d20a2016544840f9c1fffd8a064e02ff26e226fbfae769c6f2412b69b604121`  
		Last Modified: Sat, 27 Jan 2024 10:32:41 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc00ee35586dfd76bcfb6ffa9fe2245d6a7b82340e071ab3130f464e3520138`  
		Last Modified: Sat, 27 Jan 2024 10:32:42 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0d4a5187eb7e448f99c64bc131b4c4bc95ee11af25d9ebb02182fd24c604f5`  
		Last Modified: Sat, 27 Jan 2024 10:32:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:219c0df7438799198a2325e8ce7e07216774df5b86da1c6169998225c109af2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.9 KB (838888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582628a809b6391bfc8f6237d3c02fc7ebd818baece4e077b20449c0faa4e561`

```dockerfile
```

-	Layers:
	-	`sha256:7c695c98eecd72f7196c38163846b552093ddbcf87a5a292491258823221064b`  
		Last Modified: Sat, 27 Jan 2024 10:32:41 GMT  
		Size: 801.8 KB (801750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e367bd61fbafb104d3bf6d46d924f7970c784a7d8059c738a112477472e79e`  
		Last Modified: Sat, 27 Jan 2024 10:32:41 GMT  
		Size: 37.1 KB (37138 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:77dbdbdb2453205e6ecd9a00bff377c65778a44013d808f11d8452a1370cd3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101481025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce1e57c6281ba37271ed9afcc31e087e79290ed75015dae4d3c5ed48b31243a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=13
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=13.13
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=8af69c2599047a2ad246567d68ec4131aef116954d8c3e469e9789080b37a474
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 Dec 2023 00:27:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
STOPSIGNAL SIGINT
# Fri, 22 Dec 2023 00:27:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98867b7d9ef52d8ea690ad6ab7a1162c3ffb223f498cfe46c5a0c19b26b5df4a`  
		Last Modified: Sat, 09 Dec 2023 02:05:53 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca1d0e320956171da67959a489db8954c94e3093132a48ee544fcaf765d7784`  
		Last Modified: Sat, 09 Dec 2023 02:05:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560a49d225a06eb054d3c0a36dae94d7827f3c4ed473ed025001425682bec061`  
		Last Modified: Wed, 13 Dec 2023 01:31:47 GMT  
		Size: 98.2 MB (98222378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa582f2389d6e684e18a51948d2d9d219cb9977b8133c2e92cd3561f3f1fc53`  
		Last Modified: Wed, 13 Dec 2023 01:31:45 GMT  
		Size: 9.0 KB (9026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8b6e7e682ca5daea1c8a4b6df63f01fa8f86591ddf99ebbbb39f38b6d791c7`  
		Last Modified: Wed, 13 Dec 2023 01:31:45 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7722839ca55ab6b26d2aec58a465434d8948c20f8f291807f8c8046f70f01b07`  
		Last Modified: Wed, 13 Dec 2023 01:31:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2432e269bca78eacee825ec5e2b084ca6f1855ba0564ae162a64ae7e037b3f22`  
		Last Modified: Fri, 05 Jan 2024 02:17:56 GMT  
		Size: 5.4 KB (5425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e58025dbcd820016100ebf9535da645ffa4ce956cabeebe3a67ca945a5d7002`  
		Last Modified: Fri, 05 Jan 2024 02:17:56 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:ffd7a9d499c935d7d4391c0d469ddb564bb6f82fee0c29d746557306d20bdb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.2 KB (840213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ce17e3a84dce526fc9884452203f8a89d0eea90be0f4d59a95d04143e5997a`

```dockerfile
```

-	Layers:
	-	`sha256:36dc5d874692b7795cc731b243f9a15b4a730de977808f0143e9b6782c0280f1`  
		Last Modified: Fri, 05 Jan 2024 02:17:56 GMT  
		Size: 803.1 KB (803125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bda04d7d796703333abbe64e0de8b7b608da0d732519603aa1cdcc0fbda8da62`  
		Last Modified: Fri, 05 Jan 2024 02:17:56 GMT  
		Size: 37.1 KB (37088 bytes)  
		MIME: application/vnd.in-toto+json
