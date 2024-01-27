## `postgres:alpine`

```console
$ docker pull postgres@sha256:b863db26de1e793b67e243ef9215c6a7eb45238d1a52f1294cb5529f1f592bf5
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

### `postgres:alpine` - linux; amd64

```console
$ docker pull postgres@sha256:c32324cb8177cca81c5fc275bcb9845049452bd15515208805e83c4271999f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95690409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fc9aa92741f4db4e66d3cb08dc9580332a8cfddb7908afabb051ae0db96ef1`
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
ENV PG_MAJOR=16
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=16.1
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=ce3c4d85d19b0121fe0d3f8ef1fa601f71989e86f8a66f7dc3ad546dd5564fec
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:064ad39e66f151042410bb3375001389225c9b370d21275ee0d77ed3881572ca`  
		Last Modified: Sat, 27 Jan 2024 00:57:58 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969d8f83b78aad0df34e1b98580c907fafc68fcaeaf269f5b45756f18e24aeb6`  
		Last Modified: Sat, 27 Jan 2024 00:57:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f4346dbb5e28e0b8eb8136e782d7a31178d30866e685d1ed6f61ec8c473903`  
		Last Modified: Sat, 27 Jan 2024 00:58:00 GMT  
		Size: 92.3 MB (92264841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f74a286f0f5dfba1f716dc4daeb3b13dbead08ea569ea9f5b282b8c1a27f9b`  
		Last Modified: Sat, 27 Jan 2024 00:57:58 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a920b3af04e1ecdb49c0c88a89d5ff5df8d9a516af703b88ce92d44ffcfa1c27`  
		Last Modified: Sat, 27 Jan 2024 00:57:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5975d00404a2bd33d5c10cfca275bdc733d30dc1669f44f4ce30d59a2dd9f02a`  
		Last Modified: Sat, 27 Jan 2024 00:57:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c41f96aa7076a2fce08d76f6a4e08c9d8d1711a9a4e0a17a2df74e51227686`  
		Last Modified: Sat, 27 Jan 2024 00:57:59 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71444cd8dc149fe0bcdc0c6d5fc769282b4d083b13a682bfe1ab04c944993fda`  
		Last Modified: Sat, 27 Jan 2024 00:58:00 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:c13020acfdbc3778017b2805f03c26f7e77c9dc6ab6448217f506f0ef23ab082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **846.3 KB (846302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6858e1b7ff7b99a6bd1c4201bfc3dbce47c51a751cbf1439eca446a069eb687c`

```dockerfile
```

-	Layers:
	-	`sha256:e8da35db6d7b766ff6b4801017faa4a4b2b2842d650d38cb3b02b0d1e78cad26`  
		Last Modified: Sat, 27 Jan 2024 00:57:58 GMT  
		Size: 807.9 KB (807929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21692e3bd251907bd14558a1443ee709ffec4b35d1902ac4b39d895e5fc8f31d`  
		Last Modified: Sat, 27 Jan 2024 00:57:58 GMT  
		Size: 38.4 KB (38373 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:5745a6c93137315da668302d6d39fb54d5b8e4908322218d7cfe282f37a243c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94410268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edcb99966e7406bf8209562228e952f44fbb1cf2b73d7ac8747f921f83490bd6`
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
ENV PG_MAJOR=16
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=16.1
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=ce3c4d85d19b0121fe0d3f8ef1fa601f71989e86f8a66f7dc3ad546dd5564fec
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:8ec93e4dd3397c7bd45cdf114626f1e822da7fc463c87f768aef25b32ab46f8d`  
		Last Modified: Sat, 06 Jan 2024 11:54:22 GMT  
		Size: 91.2 MB (91228277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd66103b7046b37723449f0d6852368aa3d2705ddd080252fd96db756f0f8de`  
		Last Modified: Sat, 06 Jan 2024 11:54:19 GMT  
		Size: 9.6 KB (9563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca97dcc8b6aa20ccc3100f021ea42b38abd1a5946be12c46acb22e06edda00d`  
		Last Modified: Sat, 06 Jan 2024 11:54:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0599d82cf51ef3fbdbe5e3a10abe19a7d135794557214c429c2aa3ea82a0f114`  
		Last Modified: Sat, 06 Jan 2024 11:54:20 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23aa60d1e37a1cdb4851e54423d8f7f013c0f63cfe21d76e03a69496ed05dd0e`  
		Last Modified: Sat, 06 Jan 2024 11:54:20 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad802dc47987ea2e0b17e3885eebf2e506b1d7d910971030ac767c67c210119`  
		Last Modified: Sat, 06 Jan 2024 11:54:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:8641bd8f04566d2fa2d0fd5c09f3cb9cc8401a3b34657cfb26da11fc82c71a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54784c925fb99339e032142423b547d2cb2b66b984736255ca40fa6af90ab9ee`

```dockerfile
```

-	Layers:
	-	`sha256:ad50fb6f70e92b4c423109fcf8cc76bdc332071491be5997a21307df3f871479`  
		Last Modified: Sat, 06 Jan 2024 11:54:19 GMT  
		Size: 38.2 KB (38156 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:71ecfd7ef1f0c8d14170dd3bc02c9dc89a61f95c852b48716e14a43660310b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88853224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a69e8bd63e064d441e5a8bf0ef0a33279db784f39703537715cd3305e9a50a4`
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
ENV PG_MAJOR=16
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=16.1
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=ce3c4d85d19b0121fe0d3f8ef1fa601f71989e86f8a66f7dc3ad546dd5564fec
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:bfbb5d183a884b3bf77864fa2b775171c4ba5c16513ddd348d57ff7bce07a48e`  
		Last Modified: Sat, 27 Jan 2024 16:43:22 GMT  
		Size: 85.9 MB (85917482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed4c057b0b27d1e5a870539bb1ac2daaa21ae46404de31c4914426bd982ad4b`  
		Last Modified: Sat, 27 Jan 2024 16:43:21 GMT  
		Size: 9.6 KB (9566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5e63a08255415da104cb9fc5a4b82b945be190c823987006edcc34a07ae147`  
		Last Modified: Sat, 27 Jan 2024 16:43:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5590ef17d40494d030c4de9e907716ed60adb72212d88bb46c03e4b940cd3c1`  
		Last Modified: Sat, 27 Jan 2024 16:43:21 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4a63c0b48a784c13ed1e4d5a4de7e52062a860cd78b6aa1ff2ed6382f752f7`  
		Last Modified: Sat, 27 Jan 2024 16:43:22 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af22907b9e87254dafd9525bb4dbc81c0423062714757a9f4cda71b6a8b572f`  
		Last Modified: Sat, 27 Jan 2024 16:43:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:120b60d701fa0ac03bfd08c7a5ddb3903e0665b7bb5e369424499982b98ca9fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **846.4 KB (846352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71b2222bffcb721d49c195c0168eddb30376d65f44f2aef47500e2a9fff1cbe`

```dockerfile
```

-	Layers:
	-	`sha256:6fcecb16c0da57e53c9e9473a91cbb34238ef258541b5e9f0e32b7c80948f391`  
		Last Modified: Sat, 27 Jan 2024 16:43:20 GMT  
		Size: 808.0 KB (807981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74aa40d39bf94e4d2a785f7417aa92a0f683f6f951e74a87a117e3a2cff0385e`  
		Last Modified: Sat, 27 Jan 2024 16:43:20 GMT  
		Size: 38.4 KB (38371 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:1a02585cc97e942fb814c85a5c98924510344e472b31c65b7204fb89e48f6f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94441285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a121fb3e20776dd8dc2e74f3fe5453b9209fb8e68f132eff38dc70188bcc86`
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
ENV PG_MAJOR=16
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=16.1
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=ce3c4d85d19b0121fe0d3f8ef1fa601f71989e86f8a66f7dc3ad546dd5564fec
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:eec44e821ea0eec8e21b2f03ff892b24c41f5cafd0990be4e3d4a4f2146d9beb`  
		Last Modified: Wed, 13 Dec 2023 02:39:24 GMT  
		Size: 91.1 MB (91076639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00862d56f995a615bbac1ad730089473f1136f7a3936019f99237031d6f6ec94`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 9.6 KB (9562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2572a4326bc7c4fc3e5b3d09db7e53adf33d63acbf73658b316f26c3e5acc1fc`  
		Last Modified: Wed, 13 Dec 2023 02:39:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3276f3132639a74b449c4edc63c4a46308425614cca5e683f10f16d4018956`  
		Last Modified: Wed, 13 Dec 2023 02:39:22 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef6950083f8bf34af99af8abbdb625e282098d8ca51b990c9f55ae43b2cef2c`  
		Last Modified: Fri, 05 Jan 2024 02:25:17 GMT  
		Size: 5.4 KB (5425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bb66e4fbb7595f983cf7ded21cc9d910f5cc67719e10d684089df898b126af`  
		Last Modified: Fri, 05 Jan 2024 02:25:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:a6c6889254bfe336084d679625af047d023d63ba796db281fc05533652e53f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **846.2 KB (846159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6c924f1b50215886d0185c85c95741dac1e35dd5c49b20264604df27a845af`

```dockerfile
```

-	Layers:
	-	`sha256:6f3576b6fc57c08d16730daea3d03b0b1762d18ab5be9cfadc8aad79fc21b6bc`  
		Last Modified: Fri, 05 Jan 2024 02:25:17 GMT  
		Size: 807.9 KB (807938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a93b657a9bfb2fa071da10cbde462c3b25bfcbcdb8a0a79ae0edb32760524abd`  
		Last Modified: Fri, 05 Jan 2024 02:25:17 GMT  
		Size: 38.2 KB (38221 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine` - linux; 386

```console
$ docker pull postgres@sha256:e8b1569f820dc4785f041eb161f8439dcb30f79e014e5ccafa7f288be6bdd4ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (100965533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b722a1e82bfd0a614d5496cbad3ff59fea4f324d273183562f44a641fd3c665`
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
ENV PG_MAJOR=16
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=16.1
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=ce3c4d85d19b0121fe0d3f8ef1fa601f71989e86f8a66f7dc3ad546dd5564fec
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:5b3eaa6d309b500e7b5376937b26caaf7952afdc8f6cb932b9ee72d49487eaf9`  
		Last Modified: Sat, 27 Jan 2024 01:58:12 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a3190c26e304f0767fe70beccde5568a809a6156c902aa4e617084d499abcc`  
		Last Modified: Sat, 27 Jan 2024 01:58:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd66ab5276eaf70ead3d08bd71e6b08986d51c05ab9569ed89911f9384b30cd`  
		Last Modified: Sat, 27 Jan 2024 01:58:46 GMT  
		Size: 97.7 MB (97704598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e988fe022631eeccf44a8757f223821c42aaba04b8f03240f038af546a318fc0`  
		Last Modified: Sat, 27 Jan 2024 01:58:44 GMT  
		Size: 9.6 KB (9564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb67e7419cc1cf4be7577e4e91c05fb0e1af4a8838d75248ff755ce75711b89`  
		Last Modified: Sat, 27 Jan 2024 01:58:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621c6c6794d5bb742082404306e3e260746d2a1e3b4a34ddb099a3b7db2d67f4`  
		Last Modified: Sat, 27 Jan 2024 01:58:44 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd96a7cb84260c01b8b55431fb902f9c47f00bf80aac5b33311d060f13b3ae62`  
		Last Modified: Sat, 27 Jan 2024 01:58:44 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a5ba06d585578eb0c7b09f046f81f75c2d9c1e71a30ddb01318aff02e4c2c0`  
		Last Modified: Sat, 27 Jan 2024 01:58:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:f47f25a0c0d39cda1ee482fa01a81621d4c738f6ec7723954716fd67e0e32b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **846.2 KB (846216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df7e973ab342f87684638f42b57d847f09e081a7edb8101925e3e10b1d031f5`

```dockerfile
```

-	Layers:
	-	`sha256:977b49bf3581edd34d3f0b1f954aaf999444a1cc01523cd882a0621ab71f15a2`  
		Last Modified: Sat, 27 Jan 2024 01:58:43 GMT  
		Size: 807.9 KB (807894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6606fa2620ce6a82c5865e4b2bd6ca9c3f1a89ecccda6687f15d559036c750b8`  
		Last Modified: Sat, 27 Jan 2024 01:58:43 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:ad46faf5acbe2c6e122181620824934ea7c554148c100f9216834f7ea7aea7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.3 MB (100321710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8b41d957ff1a65afdedecd4a3b5afc39573301d79ea00a72bd21daf56c52b1`
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
ENV PG_MAJOR=16
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=16.1
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=ce3c4d85d19b0121fe0d3f8ef1fa601f71989e86f8a66f7dc3ad546dd5564fec
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:bd71f3f762d326dac6582a8ff3a53ddee8b7031111c623ec986e6f090551d9bc`  
		Last Modified: Sat, 27 Jan 2024 10:14:09 GMT  
		Size: 96.9 MB (96946510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c239ce4fc35a222313a11196acb25b13a37bf4b90d2426afec3c6935df1f1c`  
		Last Modified: Sat, 27 Jan 2024 10:14:07 GMT  
		Size: 9.6 KB (9571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4484a1e30c12e2c46d20d2e876dcd08de316f3275d63338163476297350e81`  
		Last Modified: Sat, 27 Jan 2024 10:14:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023bde3bd5becd780bdbae32a886c05f35042891f36c6f752335bbcdfb66223d`  
		Last Modified: Sat, 27 Jan 2024 10:14:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87c1bb9b71082b7e8125e43ad1017b3a040394f02b4cf7fc0c602a330c3e26d`  
		Last Modified: Sat, 27 Jan 2024 10:14:08 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ac151758b2a13f39aa2a8f20c748be3f51f5cef8953d9f1c58d0f098a18794`  
		Last Modified: Sat, 27 Jan 2024 10:14:09 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:0f6b059a4424aa6251d6438e4c508c0a3bbe42d11a88b402ff2b4138fab78350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.2 KB (843193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c369be7ef99a77e4e0194447318f2022d4fe28d9756eb1d1f243c2d98e3015`

```dockerfile
```

-	Layers:
	-	`sha256:cd041ffe2082265a8111dcd704902f927899f100ffddbb51a8e7bf7a265725df`  
		Last Modified: Sat, 27 Jan 2024 10:14:07 GMT  
		Size: 804.9 KB (804924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6eda5d46042df27a669a777cbbeb567b6b6c52364f3c96b5f84dea2160aeed8`  
		Last Modified: Sat, 27 Jan 2024 10:14:07 GMT  
		Size: 38.3 KB (38269 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine` - linux; s390x

```console
$ docker pull postgres@sha256:a2bd114baeb2257605dd2be65fbf7562a2b2ada441daa189798281d3141aeb72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104598965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7d7c46136d13e8c560c920d9e8a5a2ade4af5a2f829e200842c68fed383f27`
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
ENV PG_MAJOR=16
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=16.1
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=ce3c4d85d19b0121fe0d3f8ef1fa601f71989e86f8a66f7dc3ad546dd5564fec
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:a7f7010d76ceff0dd4d000eb71ffad9ed7a5b575adfbe651d85a97439db3c560`  
		Last Modified: Wed, 13 Dec 2023 00:46:10 GMT  
		Size: 101.3 MB (101339778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686b71a99b6050515a9c6d7c8e1fad4d4fc041f26d668347d98acd8bb432cc23`  
		Last Modified: Wed, 13 Dec 2023 00:46:05 GMT  
		Size: 9.6 KB (9567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00267657344730f1fffe25c3b23bc0234549149769ff7fdceb16e66bf3f96353`  
		Last Modified: Wed, 13 Dec 2023 00:46:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049476ec6f047890d876f7e6b687ce80a4acec89f0edc0b47d3a2d69fd8e28fc`  
		Last Modified: Wed, 13 Dec 2023 00:46:06 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a417c52d8110a0921d38e03f402f7b4fe4e07736e54aaa6d2525267d20a642a`  
		Last Modified: Fri, 05 Jan 2024 02:08:19 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9cc0f1d88a9020c7206843d54c3356308607af6010592c9ba4ddc1e287fb84`  
		Last Modified: Fri, 05 Jan 2024 02:08:19 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:c7cba7663e58e105172cd223e6beee451c04957d386c0ca544365367a3b64882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **844.5 KB (844500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17d426b648d3f1b743ea9e4748edf916da6c53a0881eb243a0687f9c0c94787`

```dockerfile
```

-	Layers:
	-	`sha256:773f823f04623f01b7d53ebf37d52929422b098d99a31264f15fa51a8040ecbd`  
		Last Modified: Fri, 05 Jan 2024 02:08:19 GMT  
		Size: 806.3 KB (806287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8bfb8d13d7ad63e5d72a543e86c9af30ca02659df5c53c4cc546989cfa02837`  
		Last Modified: Fri, 05 Jan 2024 02:08:18 GMT  
		Size: 38.2 KB (38213 bytes)  
		MIME: application/vnd.in-toto+json
