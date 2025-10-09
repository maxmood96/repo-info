## `postgres:13-alpine3.21`

```console
$ docker pull postgres@sha256:a9f28a7c7adc124bacafaceb2cbbe091ababa2c976653bf6636091b69f17cf76
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

### `postgres:13-alpine3.21` - linux; amd64

```console
$ docker pull postgres@sha256:247fba78433d95faf888395863c8b34e7426a2f78ddf40ea51c75a80a5138f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (109014755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e0c7a5279c359d2b3a46893689ee56bf9cb438dec5cd4d3841bd7f76c34d87`
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
ENV PG_MAJOR=13
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=13.22
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:fa331c41cc40880a7a4f71fd6e62ee53ce08da54c5a87bd6f59b10cc06b1ef31`  
		Last Modified: Wed, 01 Oct 2025 00:35:15 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec286582ca0a6c204186e56ea6f236a92af8a9e6bdfe988144d5e7d5d45df731`  
		Last Modified: Wed, 01 Oct 2025 00:35:16 GMT  
		Size: 915.4 KB (915354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4720e4f9f4d27513cb0de7d3d03170bc5ab3f6148534451a9652df00fc24bf`  
		Last Modified: Wed, 01 Oct 2025 00:35:16 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc56f8ca250777f523bdebd74c72d359cc5bc2e1ca0556bcc07f841fc1de056`  
		Last Modified: Wed, 01 Oct 2025 00:35:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd945bab4612a414b1e50311b835fd55697dd9712ad57835124083569bd59a2`  
		Last Modified: Wed, 01 Oct 2025 00:35:33 GMT  
		Size: 104.4 MB (104445146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e70d70d3c6afdf6b85cccbbb8783d5f0adc0e06b3d1408ba4c5e8ed8de51ea4`  
		Last Modified: Wed, 01 Oct 2025 00:35:15 GMT  
		Size: 9.0 KB (9016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da77946285f3dbb0b52445dc76ab5f21c33be4fa0a4eba45813d7b5f9a4d80c8`  
		Last Modified: Wed, 01 Oct 2025 00:35:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745d715f8cdbcbd3172ab7f076ff772cc08a83dfa2aa1869d565747353a1889c`  
		Last Modified: Wed, 01 Oct 2025 00:35:15 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fa6570c24df4e86b8f6e1e9ee396c6c4c97e31619c4cc6af7ea4dccb8bb043`  
		Last Modified: Wed, 01 Oct 2025 00:35:15 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03998b05c248f9d92cbccee44aa51fa8ce93214f79d05b5dae82117809162b0a`  
		Last Modified: Wed, 01 Oct 2025 00:35:15 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:27bcd521c3bcf46b078721838a0dabec808856970b6207295e03b1bd8d2453a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.8 KB (638764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c195929cd08abf221e89f47a41e0dd513c53ba1b46317f7ede17512652791e81`

```dockerfile
```

-	Layers:
	-	`sha256:166de501d86dce31bdb19451380b112e944a3c7676c82b5f2f828b2885288ac2`  
		Last Modified: Wed, 01 Oct 2025 14:07:34 GMT  
		Size: 595.6 KB (595557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa47a59127ea918e0963877d42bd6099dc8f222aafd478c16705bcf94067852d`  
		Last Modified: Wed, 01 Oct 2025 14:07:35 GMT  
		Size: 43.2 KB (43207 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.21` - linux; arm variant v6

```console
$ docker pull postgres@sha256:5b34bcfa7ac7ea87e4d258b29a71002d8feec1bb3f2fc0e52e4233777a63eef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86390602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5186e67bbf3c49a677e11b11af9a59b183de761001327dbcf52d22b93493bbb0`
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
ENV PG_MAJOR=13
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=13.22
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:e722e26bd74a5f98b016951fb9953b6f5fd323e4468b051deb03725a97a90136`  
		Last Modified: Wed, 08 Oct 2025 22:09:03 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce58cb247bf5fce041f83c1605e8167431a15c1ca8715d051fe090b3411c10c`  
		Last Modified: Wed, 08 Oct 2025 22:09:04 GMT  
		Size: 886.1 KB (886102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3348b21afe757981ee322e84b9d5185a63ef1406b120e80c384cdfe0b5dfd9bb`  
		Last Modified: Wed, 08 Oct 2025 22:09:03 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c06654338d6fc4b4038d1c116015810936598a7fb44118f26b33d08c5d75ab0`  
		Last Modified: Wed, 08 Oct 2025 22:09:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b330789e26115e3c4b486acc56834d4b4c13364234b7d18e6642700ac5ac86`  
		Last Modified: Wed, 08 Oct 2025 22:09:12 GMT  
		Size: 82.1 MB (82122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961f6a2036f8c7ab27087e9c56c0856ef7356971d4731a999a1a8610a656ff81`  
		Last Modified: Wed, 08 Oct 2025 22:09:04 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3e16383a64a50e1a41e0d7a31b10398beaa6f8d74c4eff6b09f7d671182485`  
		Last Modified: Wed, 08 Oct 2025 22:09:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941fceb142a3d5d0a75487ad5eb589a3502f08db0c5ac232fc487221b975d57b`  
		Last Modified: Wed, 08 Oct 2025 22:09:04 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb47221e96e84ab72e6642ec63dc3d7f7c95a2c25fefac85d7e3168850a95d1f`  
		Last Modified: Wed, 08 Oct 2025 22:09:04 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2125dba665129f6369bebd3cf0ea256d35627f97ad2107f0562fad218422bb72`  
		Last Modified: Wed, 08 Oct 2025 22:09:04 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:0c168f69d139a358ed42b9084739af0d0725b8624cb66618fe509037a62ee5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 KB (43154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5716b1ab0a27118f71380e25b6de9d9b67372bd816bf0d6e8861ce8c85f33ca`

```dockerfile
```

-	Layers:
	-	`sha256:d5331e2cd2095e3469c5e685f8d2e55d826388d6af8a1e6fdd803ad1b971b596`  
		Last Modified: Wed, 08 Oct 2025 23:07:47 GMT  
		Size: 43.2 KB (43154 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.21` - linux; arm variant v7

```console
$ docker pull postgres@sha256:208fd0ea267d8304e46f727f96cf4033237f45bea412989dc518e26ff2d39929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83473847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebfa99173e8288e9c1355395ebebc95dd8cf55895e1c7168fd19d57a6dbded9`
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
ENV PG_MAJOR=13
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=13.22
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:34aa3b409b096e8b8ffde508dba16313cb1744d6c7d8e7c36c3b021736c818ed`  
		Last Modified: Tue, 30 Sep 2025 23:18:21 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb19f035f59e66f84f0e275ab510050468faf58b7362a0ba24fce5803dc505ec`  
		Last Modified: Tue, 30 Sep 2025 23:18:21 GMT  
		Size: 881.7 KB (881733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add3540e5efb47a35347bb967683b8edf9ec07a878417d030b09ac5f30a67df6`  
		Last Modified: Tue, 30 Sep 2025 23:18:22 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c14f368ea6bc060345be99f5b7152f6c59d1fb40a26da262129e72266e05054`  
		Last Modified: Tue, 30 Sep 2025 23:18:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8276bfbd1b12f740bd8a7984fbd46d759956f98517987712e5b4b94057ace1`  
		Last Modified: Tue, 30 Sep 2025 23:18:25 GMT  
		Size: 79.5 MB (79478559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d8bd50e5c829bac518877d1653a0ff9bf028d49d59f951ee4aaa46b215025c`  
		Last Modified: Tue, 30 Sep 2025 23:18:22 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1005b50973600866f15fd046fae47f4aa79f8d9909fbd5bf974b13d6ac5ec7`  
		Last Modified: Tue, 30 Sep 2025 23:18:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0229a539400545a20b8ca80f65963ba19c71bd5493a59c08e7c80721acc5a0d3`  
		Last Modified: Tue, 30 Sep 2025 23:18:23 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833d0437fe857a5631d8151e2a7d9f51c5f8f3d1a6199956f638a391beee629b`  
		Last Modified: Tue, 30 Sep 2025 23:18:21 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46e72169d7b96c818bce76e470c9c3959aefc04410694b3eec87770ac297213`  
		Last Modified: Tue, 30 Sep 2025 23:18:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:76c74bd616f3e2145f04db11f65bb388dd083230a1b33553ae1d0806ad40e298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.9 KB (638945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62119567b55e57753a45028821ed0ddafaf5cb8d917ea49a1ab7370a238ee060`

```dockerfile
```

-	Layers:
	-	`sha256:47b0ddb6e3b9301a544b4bc46feb50f6e4c6c3d8a31ba70f8a256ffaec40281d`  
		Last Modified: Wed, 01 Oct 2025 20:08:12 GMT  
		Size: 595.6 KB (595577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5dce588ba72d8e473700cdaf75c7892ed28b38e39efb8e9f6a58f176a185720`  
		Last Modified: Wed, 01 Oct 2025 20:08:13 GMT  
		Size: 43.4 KB (43368 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:e999f6de06d3430068403efb291a2008f4ae8f429e6df7e4c53976ff016ac631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102661659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9cbcc7980d246b05b6c3cdda4b877e525a768d7a30e7869d5789478e988fd8`
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
ENV PG_MAJOR=13
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=13.22
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:9ccb25555adbc0d036c0914fa61ca53fd6722013c75f52eebafb07458f8bdb4a`  
		Last Modified: Wed, 08 Oct 2025 21:43:09 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a569c5fb3f2ba39b1e6a576c962f2bd942b11d5856f9850d707348de2483c1fb`  
		Last Modified: Wed, 08 Oct 2025 21:43:09 GMT  
		Size: 873.5 KB (873463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5d94035dc9a3051967712360f8f3ead8307a489e72747e210b66aaf690a761`  
		Last Modified: Wed, 08 Oct 2025 21:46:03 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0c6c1e587d51efc3a51b86e4c5c1a624dc7b4ab94e788824d6c16525be07f1`  
		Last Modified: Wed, 08 Oct 2025 21:46:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02de4b4e9f841cd53ec32628f0e259ace3ac9ddfc2e7dca6ccc387af96092456`  
		Last Modified: Wed, 08 Oct 2025 21:46:13 GMT  
		Size: 97.8 MB (97779165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8e97f5d6e593876f201f47149c480a8ea3ef28a22eedb84bc5058df6c05871`  
		Last Modified: Wed, 08 Oct 2025 21:46:03 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a2da73ad6461bbe3b35c3b3daf79915aaf508de43c4d37ba40aeb42c1d1fb9`  
		Last Modified: Wed, 08 Oct 2025 21:46:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdb0febd031870cb2b260f8aba9ae3144db7a6e0af0a776bb12ad4c4bfa67fc`  
		Last Modified: Wed, 08 Oct 2025 21:46:03 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3e4ba82eeae328986f5c292e5650df548fa619492ecf498c1070692080f002`  
		Last Modified: Wed, 08 Oct 2025 21:46:03 GMT  
		Size: 5.9 KB (5925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51b13389fa007a8ebe0f1fb941e5001937eadda26e27c5bef5e9613d91780a3`  
		Last Modified: Wed, 08 Oct 2025 21:46:03 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:fc47ce5d8a428134541081307899f7dc5b310c351c351466421fdd7937cf418c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.0 KB (638990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68411d019891b77364e0e7a211d133b74b779dd73339f65ef78dbdd90626abc5`

```dockerfile
```

-	Layers:
	-	`sha256:eec45af8b20ecc61fc764c75bef6a14d98ef4df3b936e24982b7f920e0492156`  
		Last Modified: Wed, 08 Oct 2025 23:07:52 GMT  
		Size: 595.6 KB (595589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2c09db7acea54de2ed9298d075a0109a5463dd3e83f9352939ca5430cb9f037`  
		Last Modified: Wed, 08 Oct 2025 23:07:53 GMT  
		Size: 43.4 KB (43401 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.21` - linux; 386

```console
$ docker pull postgres@sha256:fcdab408ddeafe68f1c485fff78af8c7c249d28b4d4b51221addc47f14e5ffe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112828568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bcb72aee8390c57d692099d2482e3bd760f6055e4b8f204db316aac4b040350`
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
ENV PG_MAJOR=13
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=13.22
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:ff5826abbabf74905b17156fa4c7172d2b65cb1a5c6840d6606fff9bae2433a8`  
		Last Modified: Wed, 08 Oct 2025 21:41:21 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44ad1fac27a68bb4902dd3b79f123365b6d0658cbce4602c828359c98c02ac1`  
		Last Modified: Wed, 08 Oct 2025 21:41:22 GMT  
		Size: 890.6 KB (890612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95fe26efb842ca0fa6f2b6a8b7aef37258fd5ae837aee8275026d186dd60edb`  
		Last Modified: Wed, 08 Oct 2025 21:41:21 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab843ccf34aec7f59178713c580ed4fd1156f74a75544f79f791bd204aebcf30`  
		Last Modified: Wed, 08 Oct 2025 21:41:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7961b76902cc01f8e666c89ff0faaf92b2cfb3a16a78efe81d925338cc4fbb5`  
		Last Modified: Wed, 08 Oct 2025 21:41:27 GMT  
		Size: 108.5 MB (108456576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685787f8ca653e4aeb87dfd0aa626a92c808941802807d6e9817e1de36a24641`  
		Last Modified: Wed, 08 Oct 2025 21:41:21 GMT  
		Size: 9.0 KB (9012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5af08e4ce6b958312c1a5412a2a181834e86a75201b86e11d3788ab0dcc031`  
		Last Modified: Wed, 08 Oct 2025 21:41:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2495e531b4eb2bbd69f162c098422169fefd7128027f3b6522307567584c36`  
		Last Modified: Wed, 08 Oct 2025 21:41:21 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164bbb28a6e43ceb4e51bef6a83766203a0cb8d49a4a3974e52be400f0c93aff`  
		Last Modified: Wed, 08 Oct 2025 21:41:21 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bec8414eb477451498efba8c920457fced1a2d73eefb286cc624f55d9cd7934`  
		Last Modified: Wed, 08 Oct 2025 21:41:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:2cd65ee8518c8ea83529518bf8b8b6e94c55f253cd8b3845e45669b4a8abd35c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.7 KB (638711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b644b320af1632a306bebd0e517aa33ab2338dcb75cdb60e90dcc05e2d801ac0`

```dockerfile
```

-	Layers:
	-	`sha256:2a5ba8b69360a1284c2128cbb65bafa330a56daa688e1a2b9786cdc6eb7a0a61`  
		Last Modified: Wed, 08 Oct 2025 23:07:57 GMT  
		Size: 595.5 KB (595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:942b96f7e6f5e52ee9a10b53eff5bf0ce57f391c8d0ad2ac89ddb4583bb2123e`  
		Last Modified: Wed, 08 Oct 2025 23:07:58 GMT  
		Size: 43.2 KB (43169 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.21` - linux; ppc64le

```console
$ docker pull postgres@sha256:404835b1c13247091903a748e7f60f5eca5570252458ccd458d4baeb1552eca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92465353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646ca5cdc45c8f3c91b08b8f0af33290211871dbfa3487158b201ffab95b64b2`
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
ENV PG_MAJOR=13
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=13.22
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:800d26392972e3b1c0d57be3722443ea5bcb0045f2955fa4df0efdafd762df3a`  
		Last Modified: Thu, 02 Oct 2025 01:06:43 GMT  
		Size: 88.0 MB (88005767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53dd7b1303cee2c80784ad11387004f3960e4f1d37c72e752197dce852a8d1e`  
		Last Modified: Wed, 01 Oct 2025 10:13:48 GMT  
		Size: 9.0 KB (9022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f547dc1cc484474b646c9a79fcbd476454c680a0ac8363e50750cb1ec905619`  
		Last Modified: Wed, 01 Oct 2025 10:13:49 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103e58f01922ad91fa7bc579ee22d9c368470fa819962c70a4f0d33090995380`  
		Last Modified: Wed, 01 Oct 2025 10:13:48 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa06251f202a73df115c9ac5166a09d499b4a3fa8623ffca96e4d93df2a21a24`  
		Last Modified: Wed, 01 Oct 2025 10:13:48 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c855d6e44d37886a08ca6eaefadae5777d9d371a2ce2d8cb9d6e6fb2d9f3dba`  
		Last Modified: Wed, 01 Oct 2025 10:13:49 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:b046b6236ca6e8a26846a333688608b011f83c5a418ffc65f0d138345cc47e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.2 KB (635215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bbcf37cd4ea73aebc8582a2bdba535e33fd5f7d03fa5afcce32cd05d84f738`

```dockerfile
```

-	Layers:
	-	`sha256:de8502440ebb5367341f0b04fc98602f929132cacd8115c8dd0b249ec2ef96a3`  
		Last Modified: Wed, 01 Oct 2025 20:09:28 GMT  
		Size: 592.0 KB (591966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92a39e6b0a64edb9f60ed5e6bd89a4fe63a854ae6b64951aaf56b7c8033da042`  
		Last Modified: Wed, 01 Oct 2025 20:09:29 GMT  
		Size: 43.2 KB (43249 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.21` - linux; riscv64

```console
$ docker pull postgres@sha256:c925017a53cd06e32f64533455a5296d92f1766c867eff12ce978f56fb3fd8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108081464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95083c07384244eac9d6e473b2b13fa1bac8fe6df299d1f28d3109cf47de59e`
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
ENV PG_MAJOR=13
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=13.22
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:d44fcfec23634a77aeee78acca7cd2eaf0220526387012e46cd9c230bcae58dd`  
		Last Modified: Sat, 04 Oct 2025 00:20:10 GMT  
		Size: 103.9 MB (103854828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7932228fd766c1e456e1ce972e56a373e3bbc8dd84d4d57c145428cbe3ee76e7`  
		Last Modified: Sat, 04 Oct 2025 00:19:58 GMT  
		Size: 9.0 KB (9023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72339c4bd246e22415d1390cf5b53ccd19d48d7311273038fea7e6ba8532ebfe`  
		Last Modified: Sat, 04 Oct 2025 00:19:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcfa70da7a4772244d64e588c074e0d002c81fdd01df9598e9fb483908c4d84`  
		Last Modified: Sat, 04 Oct 2025 00:19:59 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed47d3bb59496010510acdea3b4adfcd7078d0b5da0452e93b3b846b9a5bf23`  
		Last Modified: Sat, 04 Oct 2025 00:19:58 GMT  
		Size: 5.9 KB (5931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca4cd419d98e27906ba6a5a5c65a2f8bf3f94afd0b54914d115d7644c0484bd`  
		Last Modified: Sat, 04 Oct 2025 00:19:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:7224edf0ff0eef39cabc549ed6c254a13c6a622954201a1fa815d793b0bebbdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.9 KB (636879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7721b0a5bd32033207b84ffaa1fc396c54e55aa0ffe910fab6ebcc986290c0`

```dockerfile
```

-	Layers:
	-	`sha256:24139dc4ef87bd251c88892ddc1c912f14f008ae0a5acdd4204d5adc14d38695`  
		Last Modified: Sat, 04 Oct 2025 02:07:39 GMT  
		Size: 593.6 KB (593624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48731dd5217e1eca3c837825d298222a60b0cd0c4fb70c097dbfd146d26b0159`  
		Last Modified: Sat, 04 Oct 2025 02:07:40 GMT  
		Size: 43.3 KB (43255 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.21` - linux; s390x

```console
$ docker pull postgres@sha256:fae540759f1ce2352a56e63234db2af6bcc0a3ae0867f491568b0d699cd051cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117251538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a9693313d938730c234dd6db79cc88635480d41d2879f8aa529b03702cffec`
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
ENV PG_MAJOR=13
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=13.22
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=d36d83dc89e625502cf6fb1d0529642ba1266bd614b4e4a41cefd1dddcf09080
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:1a57677713ec6923cd8c24ef8263b725c083b1d71a5fefa88a6d4835d73a6c1b`  
		Last Modified: Wed, 01 Oct 2025 17:00:22 GMT  
		Size: 112.9 MB (112881503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccff0b112b839094c1a515ae253be3219ccf3a7c2ff6b7fe4ffd43c88564ab1b`  
		Last Modified: Wed, 01 Oct 2025 17:00:06 GMT  
		Size: 9.0 KB (9017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7053548f86fe3beabc7b011209c837f741e6228d2837ad57a1aa37325ca1d6dc`  
		Last Modified: Wed, 01 Oct 2025 17:00:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082bd6e09192f8768e7cdca5d4284cf90336047402a58f366cfc42c282a7d31c`  
		Last Modified: Wed, 01 Oct 2025 17:00:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77257df990a4dfb8bdd53066f887e62b8ecf041c5b4c8a2791846644598dce25`  
		Last Modified: Wed, 01 Oct 2025 17:00:03 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e343410bd34b8426427cdd4125c4b2bffc0cefb45a2f7c12742359d0265325e`  
		Last Modified: Wed, 01 Oct 2025 17:00:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:08b4ec55285efbac4bacb2779aa83facc37d28f185f970ecbabcf6424c5449fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.8 KB (636813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5fb9d5ff807576b5f81173b8482dc39fd17542013d6c85742806654e00d34b4`

```dockerfile
```

-	Layers:
	-	`sha256:c877effc6aa6a2ba4e14c2975ac9564ba47658f0fd2991fee0ae375480ab1885`  
		Last Modified: Wed, 01 Oct 2025 20:08:27 GMT  
		Size: 593.6 KB (593606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc83233c5bf9ebe4d54f3e6718c66f59f3a0a9f2b5fff2d28829db90d683de5c`  
		Last Modified: Wed, 01 Oct 2025 20:08:28 GMT  
		Size: 43.2 KB (43207 bytes)  
		MIME: application/vnd.in-toto+json
